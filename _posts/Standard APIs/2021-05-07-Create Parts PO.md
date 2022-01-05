---
layout: post
title: "Create Parts PO"  
category: "Parts PO"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: Create a Parts Purchase Order within Fusion and return a Purchase Order Number
---



## Overview

The Parts Purchase Order API is used to create a Parts Purchase Order in Fusion.

When placing a purchase order the parts and quantities passed to the API are processed as an parts purchase order on the business system and, if successful, the purchase order number is returned.


**Requires Updated Fusion Version: 3.62.00 or newer**

 
### Validations for Parts Purchase Order 

-   Only 1 Purchase Order should be allowed to be passed in on the Request at a time
-   Set the Purchase Order Status to “In Process” when creating a Parts Purchase  Order via Unity. Currently this API will only support creating “In Process”  Parts Purchase Orders.
-   Set the Purchase Order Number to the “Next Inventory P/O Number” from the  Parts Tab of the Branch record that the Purchase Order is created from.
    -   Ensure to increment the number on the Branch record once pulling the   value to use on the newly created Parts Purchase Order.
-   Set the Purchase Order Source on the Fusion Purchase Order to “Unity” when a  Purchase Order is created this API.
    -   Add the PurchaseOrderSource value of “Unity” to the PurchaseOrderSource  Fusion Database Table.
-   Set the Inter-Branch Checkbox to True if the FillingLocationID field is populated indicating the user is creating an Inter-Branch Parts Purchase Order.
    -   The Backorder Priority should be set to “Inter-Branch” as well in this  scenario.
-   Set the Add User and Last Update User to the Unity Username from the setup.
-   Set the Add Date/Time and Last Update Date/Time to the current time the Parts Purchase Order was created ensuring to take the time zone offset into account.
-   If adding an Exchange Part to the Parts Purchase Order, the Inherent Core should be added as well and reflected in the totals.
-   The same part is not allowed on the Purchase Order more than once in the Line Item section.
-   If adding a Part to the Purchase Order that has a Purchase Conversion set to a value greater than 1, a check should be made to ensure the Quantity being passed in is a multiple of the Part’s Buy Package. If not the part shouldn’t be added and a message should be returned to notify the user.
-   If the Purchase Order is being created is set as an Inter-Branch Purchase Order then check the below Branch Parameters at the Filling Branch and compare against the quantity being requested from the Filling Branch to determine whether to allow a part to be placed on order or not. If a part can’t be ordered then a message should be returned to notify the user.
    -   Branch Parameter 288 - Commit Last Sell Pack in Filling Branch?
    -   Branch Parameter 300 - Allow IB Backorders from Parts Purchase Orders?
    -   Branch Parameter 301 - Only allow Request branch to request Order Point  Excess from Filling Branch?
-   If the Part that was passed in to be added to the Parts Purchase Order has an Alternate Purchase Source Part Setup for the Branch that matches the Purchase Order Branch and is set to “Always Order As” then use the Alternate Purchase Source Part when adding to the Purchase Order.
    -   The Alternate Purchase Source Order As Part Number and AP Vendor will be passed back for the specific Part Number.
    -   The Cost of the Alternate Purchase Source record should be used if the Cost isn’t passed in.
-   If the Create Parts Purchase Order API doesn’t pass in valid information in the lineItems section or if it is populated and the part isn’t validated in Fusion and causing it to not be added to the Parts Purchase Order, then the entire Parts Purchase Order shouldn’t be created in Fusion and a message should be returned.

#### Request Data Fields

| **Name**             | **Max Length** | **Required** | **Description**                                                                                                                                                                                                                                                                                                                           |
|----------------------|----------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocationID           |                | Y            | Branch or Location ID. This is the Branch in Fusion that is placing the Parts Purchase Order and ordering parts from a Vendor or another Fusion Branch. See                                                                                                                                                                               |
| Branch Helper API    |                |              |                                                                                                                                                                                                                                                                                                                                           |
| FillingLocationID    |                |              | Filling Branch or Location ID. This should only be populated when indicating this is an Inter-Branch Purchase Order. See                                                                                                                                                                                                                  |
| Branch Helper API    |                |              |                                                                                                                                                                                                                                                                                                                                           |
| APVendorID           |                | Dependent    | This is not required and should be ignored if the FillingLocationID is populated indicating that this is an Inter-Branch Purchase Order. If the FillingLocationID is not populated this should be required and should be the AP Vendor ID See                                                                                             |
| AP Vendor Helper API |                |              |                                                                                                                                                                                                                                                                                                                                           |
| OrderedBy            | 20             | Y            | This is the Fusion Username who placed the Purchase Order. The User can call the following API to get a list of Usernames they can pass in for this field. <https://unity.karmak.io/View-Users.html>                                                                                                                                      |
| SupplierID           |                |              | This is a Supplier ID setup in Fusion that identifies which Supplier the Parts are being ordered for. This isn’t required as only the AP Vendor is. See                                                                                                                                                                                   |
| Supplier Helper API  |                |              |                                                                                                                                                                                                                                                                                                                                           |
| PODate               | 10             |              | This is the Date of the Purchase Order. The format should be “YYYY-MM-DD”. If this isn’t passed in default to the current date.                                                                                                                                                                                                           |
| IsDirectShip         | 1              |              | This is a True/False field that indicates whether the Parts Purchase Order being created is Direct Ship or not. If this is set to True then the Shipping Address fields are required (except for AddressLine2). The Default should be False if not passed in                                                                              |
| lineItems            |                |              | This is the lineItems Node that will contain all the Parts that the user is looking to put on a Parts Purchase Order being created. This can contain multiple parts in in.                                                                                                                                                                |
| PartID               | 50             | Y            | This is the PartsInventoryDetailID as defined in the business system database for the Part they user is choosing to place on order. The user can call the RDA PartsInventory call to get the ID from the response to pass in this field. (https://unity.karmak.io/Parts-Inventory.html) The ID is the PartsInventoryDetailID from the Fusion Database that related to the LocationID for the PO submission. |
| Quantity             | 11             | Y            | This is the Quantity to be ordered of the Part on the Parts Purchase Order as a whole number.                                                                                                                                                                                                                                             |
| Cost                 | 11             |              | This is the Replacement Cost associated with the Parts Inventory Record in the Branch the Parts Purchase Order is created in. If this isn’t passed in then default to the current Replacement Cost of the Parts Inventory record in Fusion.                                                                                               |
| Message              | 200            |              | These are specific messages regarding the Part being placed on the Purchase Order. This can be found on the Additional Part Information Tab of the Part on the Parts Purchase Order.                                                                                                                                                      |
| Shipping             |                |              | This is the Shipping Node that will contain the Shipping Information that can be populated if the Parts Purchase Order is created as a Direct Ship Order. If the Purchase Order is not created as a Direct Ship Order the Shipping Address will be defaulted to the Branch’s Ship To Address that the Purchase Order is created in.       |
| CompanyName          | 50             | Dependent    | This is the Company Name on the Parts Purchase Order Shipping Tab. This should only be populated and required if the IsDirectShip field was set to True. This will be defaulted to the Company Name of the Branch if IsDirectShip is set to False                                                                                         |
| AddressLine1         | 50             | Dependent    | This is the Address Line 1 on the Parts Purchase Order Shipping Tab. This should only be populated and required if the IsDirectShip field was set to True. This will be defaulted to the Branch’s Address Line 1 if IsDirectShip is set to False                                                                                          |
| AddressLine2         | 50             |              | This is the Address Line 2 on the Parts Purchase Order Shipping Tab. This should only be populated if the IsDirectShip field was set to True. This will be defaulted to the Branch’s Address Line 2 if IsDirectShip is set to False                                                                                                       |
| City                 | 35             | Dependent    | This is the City on the Parts Purchase Order Shipping Tab. This should only be populated if the IsDirectShip field was set to True. This will be defaulted to the Branch’s City if IsDirectShip is set to False                                                                                                                           |
| Region               | 2              | Dependent    | This is the Region on the Parts Purchase Order Shipping Tab. This should only be populated if the IsDirectShip field was set to True. This will be defaulted to the Branch’s Region if IsDirectShip is set to False                                                                                                                       |
| PostalCode           | 15             | Dependent    | This is the Postal Code on the Parts Purchase Order Shipping Tab. This should only be populated if the IsDirectShip field was set to True. This will be defaulted to the Branch’s Postal Code if IsDirectShip is set to False                                                                                                             |

#### Response Data Fields

| **Name**                 | **Max Length** | **Description**                                                                                                                                                                                                                                |
|--------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocationID               |                | Branch ID the Purchase Order was created in.                                                                                                                                                                                                   |
| FillingLocationID        |                | Filling Location ID the Purchase Order was created to if the Purchase Order was an Inter-Branch PO                                                                                                                                             |
| PartsPurchaseOrderID     |                | Unique database ID of the Parts Purchase Order created in Fusion.                                                                                                                                                                              |
| PONumber                 |                | Purchase Order Number created in Fusion                                                                                                                                                                                                        |
| APVendorID               |                | APVendorID on the Parts Purchase Order created in Fusion                                                                                                                                                                                       |
| SupplierID               |                | SupplierID on the Parts Purchase Order created in Fusion                                                                                                                                                                                       |
| OrderedBy                |                | Fusion Username that created the Parts Purchase Order in Fusion based on the Request passed in.                                                                                                                                                |
| POTotal                  |                | Total Cost of the Parts Purchase Order created in Fusion.                                                                                                                                                                                      |
| lineItems                |                | Section that list all Parts created on the Parts Purchase Order                                                                                                                                                                                |
| PartID                   |                | This is the Parts Inventory Detail ID of the Part that was added to the Parts Purchase Order                                                                                                                                                   |
| PartNumber               |                | This is the Part Number that was added to the Parts Purchase Order                                                                                                                                                                             |
| Supplier                 |                | This is the Supplier of the Part Number that was added to the Parts Purchase Order                                                                                                                                                             |
| Description              |                | This is the Description of the Part Number that was added to the Parts Purchase Order                                                                                                                                                          |
| Quantity                 |                | This is the Quantity ordered of the Part Number that was added to the Parts Purchase Order                                                                                                                                                     |
| Cost                     |                | This is the Cost of the Part Number that was added to the Parts Purchase Order. This is not intended to be the Import Cost but rather the Landed Cost of the part if dealing with Currency Exchange.                                           |
| ExtendedCost             |                | This is the Extended Cost of the Part Number that was added to the Parts Purchase Order (Quantity x Cost)                                                                                                                                      |
| InherentCoreCost         |                | This is the Cost of the Inherent Core associated with the Part that was added to the Purchase Order when it was an Exchange Part                                                                                                               |
| InherentCoreExtendedCost |                | This is the Extended Cost of the Inherent Core associated with the Part that was added to the Purchase Order when it was an Exchange Part. This is the Quantity Ordered of the Part multiplied by the Inherent Core Cost.                      |
| OrderAsPart              |                | This is the Order As Part that is used if the Part that is added to the Parts Purchase Order has an Alternate Purchase Source record setup in a Branch that matches the PO Branch and has an “Always Order As” option set.                     |
| OrderAsAPVendor          |                | This is the AP Vendor of the Alternate Purchase Source part that was used when the part was added to the Purchase Order if it had an Alternate Purchase Source setup in the Branch of the Purchase Order with an “Always Order As” option set. |
| Messsages                |                | This message section will provide a response back regarding the Success or Failure of the Parts Purchase Order API and it’s attempt to create a Purchase Order in Fusion.                                                                      |


### POST DATA

```
/api/unity/{version}/unityapi/PartsPurchaseOrder/Create
```

### SAMPLE REQUEST

```json
{
	"LocationID": "2345644",
	"FillingLocationID": "4",
	"APVendorID": "1234",
	"OrderedBy": "JSmith",
	"SupplierID": "3456",
	"PODate": "2021-01-15",
	"IsDirectShip": "False",
	"lineItems": [{
			"PartID": "1234",
			"Quantity": "10",
			"Cost": "25.00",
			"Message": "Ordered for Stock"
		},
		{
			"PartID": "1212",
			"Quantity": "1",
			"Cost": "4.2940",
			"Message": "Ordered for Shop"
		}
	],
	"Shipping": {
		"CompanyName": "ABC Distributors",
		"AddressLine1": "1 Karmak Plaza",
		"AddressLine2": "",
		"City": "Carlinville",
		"Region": "IL",
		"PostalCode": "62626"
	}
}
```

### SAMPLE RESPOSE

```json
{
	"LocationID": "1",
	"FillingLocationID": "",
	"PartsPurchaseOrderID": "12112",
	"PONumber": "200645",
	"APVendorID": "1234",
	"SupplierID": "3456",
	"OrderedBy": "JSmith",
	"POTotal": "254.2900",
	"lineItems": [{
			"PartID": "1234",
			"PartNumber": "0218GG16",
			"Supplier": "Bendix",
			"Description": "Gasket",
			"Quantity": "10",
			"Cost": "25.0000",
			"ExtendedCost": "250.0000",
			"InherentCoreCost": "25.0000",
			"InherentCoreExtendedCost": "250.0000",
		},
		{
			"PartID": "1212",
			"PartNumber": "0218GG151",
			"Supplier": "Bendix",
			"Description": "Seal",
			"Quantity": "1",
			"Cost": "4.2940",
			"ExtendedCost": "4.2900",
		}
	],
	"messages": [
		"success"
	]
}
```
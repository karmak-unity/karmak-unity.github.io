---
layout: post
title: "Parts PO Details"  
category: "Parts PO"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: Parts Purchase Orders to get the details of all Parts on a Parts Purchase Order in Fusion.
---



## Overview
Parts Purchase Orders to get the details of all Parts on a Parts Purchase Order in Fusion.


---------------------

   
GET will be used for the call, passing in the PartsPurchaseOrderID as part of the URL for the Fusion Parts Purchase Order the user would like to see the detail parts returned for.   

 **Requires Updated Fusion Version: 3.62.00 or newer**

### RESPONSE FIELDS


| **Name**                 | **Description**                                                                                                                                                                                                           |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocationID                               | Branch ID the Purchase Order was created in.                                                                                                                                                                              |
| FillingLocationID                        | Filling Location ID the Purchase Order was created to if the Purchase Order was an Inter-Branch PO                                                                                                                        |
| PartsPurchaseOrderID                     | Unique database ID of the Parts Purchase Order created in Fusion.                                                                                                                                                         |
| PONumber                                 | Purchase Order Number created in Fusion                                                                                                                                                                                   |
| APVendorID                               | APVendorID on the Parts Purchase Order created in Fusion                                                                                                                                                                  |
| SupplierID                               | SupplierID on the Parts Purchase Order created in Fusion                                                                                                                                                                  |
| OrderedBy                                | Fusion Username that created the Parts Purchase Order in Fusion based on the Request passed in.                                                                                                                           |
| POTotal                                  | Total Cost of the Parts Purchase Order created in Fusion.                                                                                                                                                                 |
| lineItems                                | Section that list all Parts created on the Parts Purchase Order                                                                                                                                                           |
| PartID                                   | This is the Parts Inventory Detail ID of the Part that was added to the Parts Purchase Order                                                                                                                              |
| PartNumber                               | This is the Part Number that was added to the Parts Purchase Order                                                                                                                                                        |
| Supplier                                 | This is the Supplier of the Part Number that was added to the Parts Purchase Order                                                                                                                                        |
| Description                              | This is the Description of the Part Number that was added to the Parts Purchase Order                                                                                                                                     |
| Quantity                                 | This is the Quantity ordered of the Part Number that was added to the Parts Purchase Order                                                                                                                                |
| Cost                                     | This is the Cost of the Part Number that was added to the Parts Purchase Order. This is not intended to be the Import Cost but rather the Landed Cost of the part if dealing with Currency Exchange.                      |
| ExtendedCost                             | This is the Extended Cost of the Part Number that was added to the Parts Purchase Order (Quantity x Cost)                                                                                                                 |
| InherentCoreCost                         | This is the Cost of the Inherent Core associated with the Part that was added to the Purchase Order when it was an Exchange Part                                                                                          |
| InherentCoreExtendedCost                 | This is the Extended Cost of the Inherent Core associated with the Part that was added to the Purchase Order when it was an Exchange Part. This is the Quantity Ordered of the Part multiplied by the Inherent Core Cost. |
| OrderAsPart                              | This is the Order As Part that is selected from the Alternate Purchase Source file to use when ordering the main part on the specific Parts Purchase Order.                                                               |
| OrderAsAPVendor                         | This is the AP Vendor of the Alternate Purchase Source part that was used when ordering the main part on the specific Parts Purchase Order.                                                                               |
| Messsages                                | This message section will provide a response back regarding the Success or Failure of the Parts Purchase Order API and it’s attempt to create a Purchase Order in Fusion.                                                 |


### Post

```
/api/unity/{version}/unityapi/PartsPurchaseOrder/Details/{PartsPurchaseOrderID}
```
 


#### RESPONSE

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
			"OrderAsPart": "",
			"OrderAsAPVendor": ""

		},
		{
			"PartID": "1212",
			"PartNumber": "0218GG151",
			"Supplier": "Bendix",
			"Description": "Seal",
			"Quantity": "1",
			"Cost": "4.2940",
			"ExtendedCost": "4.2900",
			"InherentCoreCost": "",
			"InherentCoreExtendedCost": "",
			"OrderAsPart": "",
			"OrderAsAPVendor": ""
		}
	],
	"messages": [
		"success"
	]
}

```
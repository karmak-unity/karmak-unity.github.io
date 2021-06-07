---
layout: post
title: "Parts PO Search"  
category: "Parts PO"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: The Parts Purchase Order Search Helper API provides a user a way to return a listing of Purchase Orders created in Fusion
---



## Overview
The Parts Purchase Order Search Helper API provides a user a way to return a listing of Purchase Orders created in Fusion


---------------------

Parts Purchase Orders have been created in Fusion and a user needs the ability to call Fusion and get a list of Parts Purchase Orders that exist in Fusion.

The following fields will be allowed to be passed in on the Request to serve as filter criteria to determine what Parts Purchase Orders the user would like to be returned.

**Requires Updated Fusion Version: 3.62.00 or newer**

### API Logic

-   POStartDate and POEndData will always default to todays date if not submitted
-   Location is required to search a date range.
-   If no location is submitted (meaning searching at a FUSION customer level),
    -   responses will be limited to a specific Date, POStartDate and POEndDate must be the same
        -   “Give me every PO with a date of today for Customer ________”
-   Responses will be limited to 1500.
    -   if the limit is reached, a message indicating the maximum number of records has been returned

### REQUEST URL

```
/api/unity/{version}/unityapi/PartsPurchaseOrder/Search
```
 


#### Request Fields: 

| Field Name | Size | Required | Default Value | Description |
|---------------------|-------------|-------------------------------------|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocationID          |             | **\*\*YES\*\*** See API Logic Notes |                        | BranchID that the Parts Purchase Order is created in.                                                                                                                                                                                                                                                                                      |
| StatusID            | 20          |                                     |                        | Status of the Parts Purchase Order in Fusion. The user should pass in the ID value which is the numeric value listed below. The description is also included for reference but shouldn’t be passed in. Valid values are; 1 = Suggested PO 2 = In Process 3 = Return In Process 4 = Finalized Return 5 = On Order 6 = Partial 7 = Received  |
| PurchaseOrderTypeID | 20          |                                     |                        | Type of Parts Purchase Order that is created in Fusion. The user should pass in the ID value which is the numeric value included below. The description is also included for reference but shouldn’t be passed in. Valid options are; 1 = Purchase Order                                                                                   |
|                     |             |                                     |                        | 2 = Return                                                                                                                                                                                                                                                                                                                                 |
|                     |             |                                     |                        | 3 = Direct Ship                                                                                                                                                                                                                                                                                                                            |
|                     |             |                                     |                        | 4 = Inter-Branch                                                                                                                                                                                                                                                                                                                           |
| APVendorID          |             |                                     |                        | AP Vendor ID of the Parts Purchase Order in Fusion                                                                                                                                                                                                                                                                                         |
| POStartDate         | 10          |                                     | Current Date           | Starting Date used to compare against the Purchase Order Date on the Parts Purchase Order in Fusion. When location is submitted, if POEndDate is passed in but no POStartDate then assume it is looking for all Parts Purchase Orders with a PO Date up to the POEndDate Date format should be YYYY-MM-DD                                                              |
|                     |             |                                     | YYYY-MM-DD             |                                                                                                                                                                                                                                                                                                                                            |
| POEndDate           | 10          |                                     | Current Date           | Ending Date used to compare against the Purchase Order Date on the Parts Purchase Order in Fusion. When location is submitted, if POStartDate is passed in but no POEndDate then assume it is looking for all Parts Purchase Orders with a PO Date after the POStartDate Date format should be YYYY-MM-DD                                                              |
|                     |             |                                     | YYYY-MM-DD             |                                                                                                                                                                                                                                                                                                                                            |
| OrderedBy           | 20          |                                     |                        | Fusion Username that ordered or created the Parts Purchase Order.                                                                                                                                                                                                                                                                          |


### Response Fields

| Name             | Max Length | Description                                                                                                                                                                                               |
|----------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| criteria             |                | This section will return the Request fields and values populated in the fields so the user can match up the Response returned with the Request for Parts Purchase Purchase Orders that was passed into Fusion |
| purchaseOrders       |                | This group will contain Fusion Parts Purchase Order(s) that are returned based on the Request passed in.                                                                                                      |
| APVendorGroup        |                | This group will return all AP Vendor information that is on the specific Parts Purchase Order being returned.                                                                                                 |
| APVendorID           |                | APVendorID on the Parts Purchase Order created in Fusion                                                                                                                                                      |
| APVendor             |                | AP Vendor on the Parts Purchase Order                                                                                                                                                                         |
| APVendorName         |                | Vendor Name of the AP Vendor on the Parts Purchase Ordser                                                                                                                                                     |
| LocationGroup        |                | This group will return Branch Information about the Branches associated with the specific Parts Purchase Order returned in the response.                                                                      |
| FillingLocationID    |                | Filling Location ID the Purchase Order was created to if the Purchase Order was an Inter-Branch PO                                                                                                            |
| FillingLocation      |                | Filling Branch of the Inter-Branch Parts Purchase Order                                                                                                                                                       |
| LocationID           |                | Branch ID the Purchase Order was created in.                                                                                                                                                                  |
| Location             |                | Branch of the Parts Purchase Order                                                                                                                                                                            |
| OrderedBy            |                | Fusion Username that created the Parts Purchase Order in Fusion based on the Request passed in.                                                                                                               |
| PartsPurchaseOrderID |                | This is the unique database ID of the Parts Purchase Order returned from Fusion.                                                                                                                              |
| PONumber             |                | Purchase Order Number created in Fusion                                                                                                                                                                       |
| POTotal              |                | Total Cost of the Parts Purchase Order created in Fusion.                                                                                                                                                     |
| SupplierGroup        |                | This group will return Supplier Information about the Supplier associated with the specific Parts Purchase Order returned in the response.                                                                    |
| SupplierID           |                | SupplierID on the Parts Purchase Order created in Fusion                                                                                                                                                      |
| Supplier             |                | Supplier of the Parts Purchase Order                                                                                                                                                                          |
| CompanyName          |                | Company Name of the Supplier on the Parts Purchase Order                                                                                                                                                      |
| Status               |                | Status of the Parts Purchase Order                                                                                                                                                                            |
| PODate               |                | PO Date of the Parts Purchase Order                                                                                                                                                                           |
| AddUser              |                | Fusion User who added the Parts Purchase Order                                                                                                                                                                |
| AddDate              |                | Add Date and Time of the Parts Purchase Order                                                                                                                                                                 |
| LastUpdateUser       |                | Fusion User who last updated the Parts Purchase Order                                                                                                                                                         |
| LastUpdateDate       |                | Date and Time the last time the Parts Purchase Order was updated                                                                                                                                              |
| Source               |                | Source of the Parts Purchase Order                                                                                                                                                                            |
| BackorderPriority    |                | Backorder Priority of the Parts Purchase Order                                                                                                                                                                |
| IsInterBranch        |                | This will display a True or False depending on whether the Parts Purchase Order returned is an Inter-Branch Parts Purchase Order                                                                              |
| IsReturn             |                | This will display a True or False depending on whether the Parts Purchase Order returned is a Return Parts Purchase Order                                                                                     |
| IsDirectShip         |                | This will display a True or False depending on whether the Parts Purchase Order returned is a Direct Ship Parts Purchase Order                                                                                |




#### REQUEST

```json
/PartsPurchaseOrder/Search?LocationID=7&POStartDate=10/13/2014
```
 
#### RESPONSE

```json
{
	"criteria": {
		"LocationID": "7",
		"Status": "",
		"PurchaseOrderTypeID": "",
		"APVendorID": "",
		"POStartDate": "10/13/2014",
		"POEndDate": "10/13/2014",
		"OrderBy": ""
	},
	"puchaseOrders": [{
			"APVendorGroup": {
				"APVendorID": "1234",
				"APVendor": "1122",
				"APVendorName": "Napa"
			},
			"BranchGroup": {
				"FillingLocationID": "",
				"FillingLocation": "",
				"LocationID": "1",
				"Location": "Carlinville"
			},
			"SupplierGroup": {
				"SupplierID": "2",
				"Supplier": "RAI",
				"CompanyName": "RainX"
			},
			"OrderedBy": "JSmith",
			"PartsPurchaseOrderID": "111564",
			"PONumber": "1101",
			"POTotal": "25.00",
			"Status": "On Order",
			"PODate": "2021-02-17",
			"AddUser": "JSmith",
			"AddDate": "2021-02-17 09:00:00",
			"LastUpdateUser": "JSmith",
			"LastUpdateDate": "2021-02-17 09:00:00",
			"Source": "Unity",
			"BackorderPriority": "",
			"IsInterBranch": "False",
			"IsReturn": "False",
			"IsDirectShip": "False"
		},
		{

			"APVendorGroup":
			{
				"APVendorID": "5634",
				"APVendor": "2356",
				"APVendorName": "Bendix"
			},
			"BranchGroup":
			{
				"FillingLocationID": "",
				"FillingLocation": "",
				"LocationID": "1",
				"Location": "Carlinville"
			},
			"SupplierGroup":
			{
				"SupplierID": "45",
				"Supplier": "BW",
				"CompanyName": "Bendix"
			},
			"OrderedBy": "JSmith",
			"PartsPurchaseOrderID": "111565",
			"PONumber": "1102",
			"POTotal": "124.87",
			"Status": "On Order",
			"PODate": "2021-02-17",
			"AddUser": "JSmith",
			"AddDate": "2021-02-17 09:05:00",
			"LastUpdateUser": "JSmith",
			"LastUpdateDate": "2021-02-17 09:05:00",
			"Source": "Unity",
			"BackorderPriority": "",
			"IsInterBranch": "False",
			"IsReturn": "False",
			"IsDirectShip": "False"
		}
	]
}

```
---
layout: post
title: "Create and Update Parts Inventory"
category: "Parts" 
icon: "icon-gear"
type: "api" 
comments: false
description:  Allow for the creation, update or retrieval of information about Fusion Parts Inventory records
---

---
---

The Parts Inventory Endpoint API in Unity will allow users to create, update or get information about Fusion Parts Inventory records.

Fusion Parts Inventory records contain the information about a specific part ranging from the Quantity Available, Description, Cost, Prices, Stock Status, Bin Location and other relevant information. The Fusion Parts Inventory Record consists of a Master Part Record which holds information such as the Part Number and Description of the Part for the entire company. The Branch Parts Inventory record holds all other information about the part that could differ by Branch for the record such as Quantity Available, Bin Location, etc… The Part Number of the Parts Inventory Record can only exist once in a specific Supplier

 
### POST Request
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/CreatePart
```

### PUT Request
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/UpdatePart
```

### GET Request
-   Retrieving Parts Inventory records in Fusion via Unity can be handled by performing a GET against the Parts Inventory or Parts Inventory Extended Data Objects in the Reports DataAccess section of the Unity Documentation located here; [Parts Inventory](https://unity.karmak.io/Parts-Inventory.html)


#### Specifications
--------------

**POST**

-   The POST method will be used to create Parts Inventory Records in Fusion.
-   Multiple Part Inventory records will be allowed in a single request call.
-   If a Master Parts Inventory doesn’t exist for the Part Number and Supplier combination then a Master record will be created.
-   If a Master Parts Inventory record does exist for the Part Number and Supplier combination then the Description of the Part Number will be used from the Master Record and the Description from the incoming request will be ignored.
-   If an existing part is found for the Branch/Part Number/Supplier
    combination, return an error since you are attempting to create a part that already exists.
-   The Parts Identity Node will be ignored in the Post when creating a Part Number
-   A response will be provided with a message section that will outline a success or any issues that prevented the part from being created.
    -   An error will be provided if the POST attempts to create a Branch Part Record that already exists in Fusion.
-   In order to create an Exchange Part, a Core Part will need to exist in Fusion so the POST on the Exchange Part will be able to reference the Core Part Number
-   A record will be written to the Parts Transactions table in Fusion when a Part is created.
-   The Fusion Username used in the Unity API call will be used as the Add and Last Update User of the Part Number created as well as the Parts Transaction record created.
-   The Date and Time the Unity API call was made will be used as the Add Date and Last Update of the Part Number created as well as the date of the Parts Transaction record created
-   The Parts Inventory record will be created in Fusion following the standard create logic of the INV90100 Parts Inventory form in Fusion outside of any specific rules listed in this section and the POST/PUT Request Fields Section below.


**PUT**

-   The PUT method will be used to update Parts Inventory Records in Fusion.
-   Multiple Part Inventory records will be allowed in a single request call.
-   Only fields that are expected to be updated should be passed in outside of the required fields.
-   In order to update an existing Parts Inventory record the user will be required to send in the Branch, Supplier and Part Number to find a match in the Parts Identity Node of the Request. If a match isn’t found an update will not be performed.
-   A response will be provided with a message section that will outline a success or any issues that prevented the part from being updated.
-   A record will be written to the Parts Inventory Transaction table in Fusion if the Quantity, Supplier, Part Number, Part Type, List Price or Replacement Cost are updated.
-   The Fusion Username used in the Unity API call will be used as the Last Update User of the Part Number created as well as the Parts Transaction record created.
-   The Date and Time the Unity API call was made will be used as the Last  Update of the Part Number created as well as the date of the Parts Transaction record created

POST/PUT Request Fields
-----------------------

| Field | Field Type | Required | Length | POST Business Rules and Defaults | PUT Business Rules and Defaults |
|----------------------------|---------|-----|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Parts Identity**         | Node    |     |       | This section will be ignored in a POST                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | This section will be used to allow the user to identify the Branch, Part Number and Supplier to be updated                                                                                                                                                                                                                                                                                                                                               |
| Branch                     | string  | Yes | 10    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | This is the Branch the Part Number will be looked up in                                                                                                                                                                                                                                                                                                                                                                                                  |
| Suppler                    | string  | Yes | 20    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | This is the Supplier the Part Number will be looked up in                                                                                                                                                                                                                                                                                                                                                                                                |
| Part Number                | string  | Yes | 50    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | This is the Part Number that will be looked up to update.                                                                                                                                                                                                                                                                                                                                                                                                |
| **Main Body**              |         |     |       | This section will be used to identify the Part Number being created                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | This section will be used to identify the fields that are updated for the Part Number identify in the Parts Identity section                                                                                                                                                                                                                                                                                                                             |
| Branch                     | string  | Yes | 10    | This is the Branch that the Part Number will be created in                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | This will be ignored in a PUT as the Branch will not be allowed to be updated                                                                                                                                                                                                                                                                                                                                                                            |
| Part Number                | string  | Yes | 50    | This is the Part Number to be created.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | This is the new Part Number that the looked up Part Number will be updated to.                                                                                                                                                                                                                                                                                                                                                                           |
| Supplier                   | string  | Yes | 20    | This is the Supplier the Part Number will be created in. The Part Number must be unique per Supplier.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | This is the new Supplier that the looked up Part Number will be updated to.                                                                                                                                                                                                                                                                                                                                                                              |
| Description                | string  | Yes | 50    | This is the Description of the Part Number. If the Supplier/Part Number is found in Fusion as a Master Parts Inventory record this value will be ignored and the Description will be used from the Master Parts Inventory record.                                                                                                                                                                                                                                                                                                                                                                                              | This is the updated Description of the looked up Part Number. This will be updated on the Master Parts Inventory record associated with the looked up Branch Parts Inventory record. The Part Description will be updated for all Branch Parts Inventory records.                                                                                                                                                                                        |
| Part Type                  | string  |     | 10    | This is the type of Part that is being created. The valid options are; Part, Exchange, Core If the Supplier/Part Number is found in Fusion as a Master Parts Inventory record, this value will be ignored and the Part Type will be used from the Master Parts Inventory record. If this value isn’t passed in or is left blank it will default to “Part” if a Master Parts Inventory record isn’t found that is set to another value besides “Part” If the value that is passed in is “Exchange” then the Core Part Number must exist in Fusion and must be populated in this request otherwise the part will not be created. | This is the type of Part that the looked up part is being updated to. The valid options are; Part, Exchange, Core If the Part is being changed to a type of “Exchange” the user will be required to provide the Core Part Number and Core Supplier of an existing part in the looked up Branch in Fusion. This will update the Part Type of the Master Parts Inventory record and change the Part Type for all Branch Parts Inventory records in Fusion. |
| Stock Status               | string  |     | 10    | This is the Stocking Status of the Part. Valid options are; Stock, Obsolete, Non-Stock If this isn’t passed in or is blank, Non-Stock will be the default.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | This is the Stocking Status that the looked up part is being updated to. Valid options are; Stock, Obsolete, Non-Stock                                                                                                                                                                                                                                                                                                                                   |
| Replacement Cost           | decimal | Yes | 19, 4 | This is the Replacement Cost of the Part. This value will be multiplied by the Replacement Cost Multiplier of the Supplier of the Part Number                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | This is the Replacement Cost that the looked up Part is being updated to.                                                                                                                                                                                                                                                                                                                                                                                |
| Price 7                    | decimal |     | 19, 4 | This is Price 7 of the Part. If this isn’t being passed in or is blank, use the Price 7 Multiplier from the Supplier record against the above figured Replacement Cost to calculate.                                                                                                                                                                                                                                                                                                                                                                                                                                           | This is the Price 7 that the looked up Part is being updated to.                                                                                                                                                                                                                                                                                                                                                                                         |
| Price 6                    | decimal |     | 19, 4 | This is Price 6 of the Part. If this isn’t being passed in or is blank, use the Price 6 Multiplier from the Supplier record against the above figured Replacement Cost to calculate.                                                                                                                                                                                                                                                                                                                                                                                                                                           | This is the Price 6 that the looked up Part is being updated to.                                                                                                                                                                                                                                                                                                                                                                                         |
| Price 5                    | decimal |     | 19, 4 | This is Price 5 of the Part. If this isn’t being passed in or is blank, use the Price 5 Multiplier from the Supplier record against the above figured Replacement Cost to calculate.                                                                                                                                                                                                                                                                                                                                                                                                                                           | This is the Price 5 that the looked up Part is being updated to.                                                                                                                                                                                                                                                                                                                                                                                         |
| Price 4                    | decimal |     | 19, 4 | This is Price 4 of the Part. If this isn’t being passed in or is blank, use the Price 4 Multiplier from the Supplier record against the above figured Replacement Cost to calculate.                                                                                                                                                                                                                                                                                                                                                                                                                                           | This is the Price 4 that the looked up Part is being updated to.                                                                                                                                                                                                                                                                                                                                                                                         |
| Price 3                    | decimal |     | 19, 4 | This is Price 3 of the Part. If this isn’t being passed in or is blank, use the Price 3 Multiplier from the Supplier record against the above figured Replacement Cost to calculate.                                                                                                                                                                                                                                                                                                                                                                                                                                           | This is the Price 3 that the looked up Part is being updated to.                                                                                                                                                                                                                                                                                                                                                                                         |
| Price 2                    | decimal |     | 19, 4 | This is Price 2 of the Part. If this isn’t being passed in or is blank, use the Price 2 Multiplier from the Supplier record against the above figured Replacement Cost to calculate.                                                                                                                                                                                                                                                                                                                                                                                                                                           | This is the Price 2 that the looked up Part is being updated to.                                                                                                                                                                                                                                                                                                                                                                                         |
| Price 1                    | decimal |     | 19, 4 | This is Price 1 of the Part. If this isn’t being passed in or is blank, use the Price 1 Multiplier from the Supplier record against the above figured Replacement Cost to calculate.                                                                                                                                                                                                                                                                                                                                                                                                                                           | This is the Price 1 that the looked up Part is being updated to.                                                                                                                                                                                                                                                                                                                                                                                         |
| List Price                 | decimal |     | 19, 4 | This is the List Price of the Part. If this isn’t being passed in or is blank, use the List Price Multiplier from the Supplier record against the above figured Replacement Cost to calculate.                                                                                                                                                                                                                                                                                                                                                                                                                                 | This is the List Price that the looked up Part is being updated to.                                                                                                                                                                                                                                                                                                                                                                                      |
| Core Supplier              | string  |     | 20    | This is the Supplier of the Core Part Number that will be associated with the Part when creating an Exchange Part This will be required if the Part Type of the request is “Exchange”                                                                                                                                                                                                                                                                                                                                                                                                                                          | This is the Core Supplier that the Core Part Number must exist in for the looked up Branch.                                                                                                                                                                                                                                                                                                                                                              |
| Core Part Number           | string  |     | 50    | This is the Core Part Number that will be associated with the Part when creating an Exchange Part. This will be required if the Part Type of the request is “Exchange” This Part must exist in the Branch the part is being created as a Part Type of “Core” and must be in the Core Supplier listed in the request.                                                                                                                                                                                                                                                                                                           | This is the Core Part Number that will be used on the looked up Part when the Part is a Part Type of “Exchange” This Core Part Number must exist in the Branch the part is being update in as a Part Type of “Core”                                                                                                                                                                                                                                      |
| Purchase Method            | string  |     | 10    | This is the Purchase Method of the Part. Valid options are; “Buy Time” and “Min/Max” If this isn’t passed in or is blank then default the value will be pulled from the Purchase Method of the Supplier of the Part being created.                                                                                                                                                                                                                                                                                                                                                                                             | This is the Purchase Method that the looked up Part is being updated to. Valid options are; “Buy Time” and “Min/Max”                                                                                                                                                                                                                                                                                                                                     |
| Bin Location               | string  |     | 20    | This is the Bin Location of the Part If Branch Parameter 329 is set to True for the Branch the Part is being created for then this will be required. It the Use Validated Bin Locations checkbox on the Enterprise Record - Parts Tab is set to true then the Bin Location being passed in must match a valid Bin Location for the Branch the part is being setup for.                                                                                                                                                                                                                                                         | This is the Bin Location that the looked up Part is being updated to If Branch Parameter 329 is set to True for the Branch the Part is being updated in then this will be required. It the Use Validated Bin Locations checkbox on the Enterprise Record - Parts Tab is set to true then the Bin Location being passed in must match a valid Bin Location for the Branch the part is being updated in.                                                   |
| Unit of Measure            | string  |     | 20    | This is the Unit of Measure of the Part being created. This must match a valid Unit of Measure setup in Fusion.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | This is the Unit of Measure that the looked up Part is being updated to. This must match a valid Unit of Measure setup in Fusion.                                                                                                                                                                                                                                                                                                                        |
| Quantity Available         | integer |     | 10    | This is the Quantity Available of the Part being Created This value must be equal to or greater than 0. If the value is greater then zero then the Quantity Adjustment Reason field is required.                                                                                                                                                                                                                                                                                                                                                                                                                               | This is the Quantity Available that the looked up Part is being updated to. If the Quantity Available is updated the Quantity Adjustment Reason field will be required as well. The value must be equal to or greater than 0.                                                                                                                                                                                                                            |
| Quantity Adjustment Reason | String  |     | 50    | This is the Quantity Adjustment Reason that will be required when the Quantity Available field is included in the request. This must match a valid Quantity Adjustment Reason in Fusion.                                                                                                                                                                                                                                                                                                                                                                                                                                       | This is the Quantity Adjustment Reason that will be required when the Quantity Available field is included in the request. This must match a valid Quantity Adjustment Reason in Fusion.                                                                                                                                                                                                                                                                 |
| EHC Code                   | String  |     | 10    | This is EHC Code that will be setup on a Parts Inventory Record in Fusion to identify an environment handling charge that will be charged at the time of selling the part. This must match a valid EHC Code setup in Fusion.                                                                                                                                                                                                                                                                                                                                                                                                   | This is the EHC Code that the looked up part will be updated with. This must match a valid EHC Code setup in Fusion.                                                                                                                                                                                                                                                                                                                                     |

#### POST JSON Request Sample
```json
[
   {
	   "PartNumber":"ks1-1",
	   "Supplier":"FLTP",
	   "Description":"Front Axle",
	   "PartType":"Part",
	   "CorePartNumber":"",
	   "CoreSupplier":"",
	   "StockStatus":"Stock",
	   "replacementCost":30.00,
	   "binLocation":"PW1",
	   "Branch":"01",
	   "Price1":25.25,
	   "Price2":25.30,
	   "Price3":25.35,
	   "Price4":25.40,
	   "Price5":25.45,
	   "Price6":25.50,
	   "Price7":25.55,
	   "ListPrice":39.00,
	   "PurchaseMethod":"Min/Max",
	   "UnitOfMeasure":"EA",
	   "QuantityAvailable":100,
	   "QuantityAdjustmentReason":"New Part to Inventory"
    },
    {
	   "PartNumber":"ks1-2",
	   "Supplier":"FLTP",
	   "Description":"Rear Axle",
	   "PartType":"Part",
	   "CorePartNumber":"",
	   "CoreSupplier":"",
	   "StockStatus":"Non-Stock",
	   "replacementCost":25.99,
	   "binLocation":"PW1",
	   "Branch":"01",
	   "Price1":25.25,
	   "Price2":25.25,
	   "Price3":25.25,
	   "Price4":25.25,
	   "Price5":25.25,
	   "Price6":25.25,
	   "Price7":25.25,
	   "ListPrice":35.00,
	   "PurchaseMethod":"Buy Time",
	   "UnitOfMeasure":"PKG",
	   "QuantityAvailable":90,
	   "QuantityAdjustmentReason":"Found Part"
    },
    {
	   "PartNumber":"ks1-3",
	   "Supplier":"FLTP",
	   "Description":"Axle Pad",
	   "PartType":"Part",
	   "CorePartNumber":"",
	   "binLocation":"PW1",
	   "CoreSupplier":"",
	   "StockStatus":"Stock",
	   "replacementCost":25.00,
	   "Branch":"01",
	   "Price1":25.25,
	   "Price2":25.25,
	   "Price3":25.25,
	   "Price4":25.25,
	   "Price5":25.25,
	   "Price6":25.25,
	   "Price7":25.25,
	   "ListPrice":35.00,
	   "PurchaseMethod":"Min/Max",
	   "UnitOfMeasure":"each",
	   "QuantityAvailable":5,
	   "QuantityAdjustmentReason":"QA-Adjustment"
    }
]
```
#### POST JSON Response Sample
```json
[
	{
		"Branch":"01",
		"PartNumber":"ks1-1",
		"Supplier":"FLTP",
		"Status":"Part was created successfully.",
		"Message":null
	}
	,{
		"Branch":"01",
		"PartNumber":"ks1-2",
		"Supplier":"FLTP",
		"Status":"Part was created successfully.",
		"Message":null
	},
	{
		"Branch":"01",
		"PartNumber":"ks1-3",
		"Supplier":"FLTP",
		"Status":"Part was created successfully.",
		"Message":null
	}
]
```

#### PUT JSON Request Sample
```json
[
    {
		"PartIdentity":
		{
			"PartNumber":"DN P562261",
            "supplier":"Q'STR",
            "branch":"01"
		},
		"PartNumber":"DN P562261",
		"Supplier":"Q'STR",
		"Description":"New Description"
    }
]
```

#### PUT JSON Response Sample
------------------------
```json
[
	{
		"Branch":"01",
		"PartNumber":"DN P562261",
		"Supplier":"Q'STR",
		"Status":"Part was updated successfully",
		"Message":null
	} 
]
```
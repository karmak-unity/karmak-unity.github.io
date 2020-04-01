---
layout: post
title: "Parts Supplier"
category: "Parts" 
icon: "icon-gear"
type: "api" 
comments: false
description:  Allow users to create, update or get information about Fusion Parts Inventory Suppliers
---

---
---

The Supplier Endpoint API in Unity will allow users to create, update or get information about Fusion Parts Inventory Suppliers.  

Suppliers allow Fusion users to segment their Parts Inventory records.  Suppliers can be used to request suggested purchase orders, setup customer pricing for parts, run reports against and many other functions.  Supplier is part of the key of the Parts Inventory record in Fusion.  


### POST Request
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/CreateSupplier
```

### PUT Request
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/UpdateSupplier
```

### GET Request
- Retrieving Supplier records in Fusion via Unity can be handled by performing a GET against the Supplier Data Object in the Reports DataAccess section of the Unity Documentation located here; [Parts Supplier](https://unity.karmak.io/Parts-Supplier.html)


#### Specifications
--------------

**POST**
-   The POST method will be used to create Supplier Records in Fusion.
-   Only one Supplier record will be allowed in a single request call.
-   The Supplier Identity section will be ignored when creating a Supplier
-   A response will be provided with a message section that will outline a success or any issues that prevented the Supplier from being created.
-   The Fusion Username used in the Unity API call will be used as the Add and Last Update User of the Supplier created.
-   The Date and Time the Unity API call was made will be used as the Add Date and Last Update of the Supplier created.
-   The Supplier record will be created in Fusion following the standard create logic of the INV9000 Supplier form in Fusion outside of any specific rules listed in this section and the POST/PUT Request Fields Section below.

**PUT**
-   The PUT method will be used to update Supplier Records in Fusion.
-   Only one Supplier record will be allowed in a single request call.
-   Only fields that are expected to be updated should be passed in outside of the required fields.
-   In order to update an existing Supplier record the user will be required to send in the Supplier in the Supplier Identity section to find a match. If a  match isn’t found an update will not be performed.
-   A response will be provided with a message section that will outline a success or any issues that prevented the supplier from being updated.
-   The Fusion Username used in the Unity API call will be used as the Last Update User of the Supplier updated.
-   The Date and Time the Unity API call was made will be used as the Last Update Date of the Supplier updated.

### POST/PUT Request Fields

| Field | Field Type | Required | Length | POST Business Rules and Defaults | PUT Business Rules and Defaults |
|-------|------------|----------|--------|----------------------------------|---------------------------------|
| **Supplier Identity**       | Node    |     |       | This will be ignored in a POST                                                                                                                                                                                                                                            | This section will be used to identify the Supplier that will be updated.                                                                                       |
| Supplier                    | string  | Yes | 20    |                                                                                                                                                                                                                                                                           | This is the Supplier that will be looked up in order to update information about the record.                                                                   |
| **Main Body**               |         |     |       |                                                                                                                                                                                                                                                                           |                                                                                                                                                                |
| Supplier                    | string  | Yes | 20    | This is the Supplier that will be created.                                                                                                                                                                                                                                | This is the Supplier that will be looked up to perform updates against.                                                                                        |
| Company Name                | string  | Yes | 100   | This is the Company Name of the Supplier that will be created.                                                                                                                                                                                                            | This is the value the Company Name field will be updated to based on the looked up Supplier record.                                                            |
| Price Group                 | string  | Yes | 20    | This is the Price Group of the Supplier that will be created This must match a valid Price Group in Fusion.                                                                                                                                                               | This is the value the Price Group field will be updated to based on the looked up Supplier record. This must match a valid Price Group in Fusion.              |
| Unit of Measure             | string  | Yes | 10    | This is the Unit of Measure of the Supplier that will be created. This must match a valid Unit of Measure setup in Fusion.                                                                                                                                                | This is the value the Unit of Measure field will be updated to based on the looked up Supplier record. This must match a valid Unit of Measure setup in Fusion |
| Replacement Cost Multiplier | decimal | Yes | 18, 6 | This is the Replacement Cost Multiplier of the Supplier that will be created. This will be used to multiply against the Replacement Cost entered on the Parts Inventory record when creating it under the specific Supplier. This value must be greater than 0.           | This is the value the Replacement Cost Multiplier field will be updated to based on the looked up Supplier record. This value must be greater than 0.          |
| Price 7 Multiplier          | decimal | Yes | 18, 6 | This is the Price 7 Multiplier of the Supplier that will be created. This will be used to multiply against the Replacement Cost calculated on the Part Number being created under the Supplier to calculate Price Level 7 on the Part. This value must be greater than 0. | This is the value the Price 7 Multiplier field will be updated to based on the looked up Supplier record. This value must be greater than 0.                   |
| Price 6 Multiplier          | decimal | Yes | 18, 6 | This is the Price 6 Multiplier of the Supplier that will be created. This will be used to multiply against the Replacement Cost calculated on the Part Number being created under the Supplier to calculate Price Level 6 on the Part. This value must be greater than 0. | This is the value the Price 6 Multiplier field will be updated to based on the looked up Supplier record. This value must be greater than 0.                   |
| Price 5 Multiplier          | decimal | Yes | 18, 6 | This is the Price 5 Multiplier of the Supplier that will be created. This will be used to multiply against the Replacement Cost calculated on the Part Number being created under the Supplier to calculate Price Level 5 on the Part. This value must be greater than 0. | This is the value the Price 5 Multiplier field will be updated to based on the looked up Supplier record. This value must be greater than 0.                   |
| Price 4 Multiplier          | decimal | Yes | 18, 6 | This is the Price 4 Multiplier of the Supplier that will be created. This will be used to multiply against the Replacement Cost calculated on the Part Number being created under the Supplier to calculate Price Level 4 on the Part. This value must be greater than 0. | This is the value the Price 4 Multiplier field will be updated to based on the looked up Supplier record. This value must be greater than 0.                   |
| Price 3 Multiplier          | decimal | Yes | 18, 6 | This is the Price 3 Multiplier of the Supplier that will be created. This will be used to multiply against the Replacement Cost calculated on the Part Number being created under the Supplier to calculate Price Level 3 on the Part. This value must be greater than 0. | This is the value the Price 3 Multiplier field will be updated to based on the looked up Supplier record. This value must be greater than 0.                   |
| Price 2 Multiplier          | decimal | Yes | 18, 6 | This is the Price 2 Multiplier of the Supplier that will be created. This will be used to multiply against the Replacement Cost calculated on the Part Number being created under the Supplier to calculate Price Level 2 on the Part. This value must be greater than 0. | This is the value the Price 2 Multiplier field will be updated to based on the looked up Supplier record. This value must be greater than 0.                   |
| Price 1 Multiplier          | decimal | Yes | 18, 6 | This is the Price 1 Multiplier of the Supplier that will be created. This will be used to multiply against the Replacement Cost calculated on the Part Number being created under the Supplier to calculate Price Level 1 on the Part. This value must be greater than 0. | This is the value the Price 1 Multiplier field will be updated to based on the looked up Supplier record. This value must be greater than 0.                   |
| List Multiplier             | decimal | Yes | 18, 6 | This is the List Price Multiplier of the Supplier that will be created. This will be used to multiply against the Replacement Cost calculated on the Part Number being created under the Supplier to calculate List Price on the Part. This value must be greater than 0. | This is the value the List Multiplier field will be updated to based on the looked up Supplier record. This value must be greater than 0.                      |


#### POST JSON Request Sample
```json
{ 
	"Supplier": "don-steph22",
	"companyName":"DSP-Stephanie",
	"pricegroup":"filters",
	"unitOfMeasure":"Gallon",
	"replacementcostMultiplier":1.000000,
	"price7Multiplier":1.123456,
	"price6Multiplier":1.234567,
	"price5Multiplier":1.345678,
	"price4Multiplier":1.456789,
	"price3Multiplier":1.567890,
	"price2Multiplier":1.678901,
	"price1Multiplier":1.789012,
	"listMultiplier":1.890123           
}
```

#### POST JSON Response Sample
```json
{
	"Status":"Successfully created supplier.",
	"Message":null
}
```

#### PUT JSON Request Sample
```json
{
  "identity":
    {
		"Supplier":"OG"                             
    },
	"Supplier": "OG123",
	"companyName":"One Gear",
	"pricegroup":"Filters",
	"unitOfMeasure":"Pack",
	"replacementcostMultiplier":1.000000,
	"price7Multiplier":1.010000,
	"price6Multiplier":1.020000,
	"price5Multiplier":1.030000,
	"price4Multiplier":1.040000,
	"price3Multiplier":1.050000,
	"price2Multiplier":1.060000,
	"price1Multiplier":1.070000,
	"listMultiplier":1.080000
}
```

#### PUT JSON Response Sample
```json
{
	"Status":"Supplier updated.",
	"Message":null
}
```

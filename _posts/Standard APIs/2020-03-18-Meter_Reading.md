---
layout: post
title: "Meter Reading"
category: "Inventory" 
icon: "icon-truck"
type: "api" 
comments: false
description:   Allow users to update the Meter Reading of an Active unit.
---

---
### Overview

The Meter Reading API will update the Meter Reading of an Active unit.

The Meter Reading API supports the PUT method.

### PUT Method
```
https://api.karmak.io/api/unity/v1/unityapi/meterreading/update
```


---

#### Specifications

**Version = API version; v1 as of June 30, 2019**

-   The Unit to update MUST be an Active Current Unit.
-   Meter Readings can be set to a value lower than the current value, to decrease the meter reading.
-   When updating Meter Type, if the input for Meter Type is not one of the valid options, the request will be rejected.
-   When updating Meter Reading, if the value is 0 or less, the request will be rejected.
-   When Update Meter Average is TRUE, the request will be rejected if:
    -   the meter reading date is back-dated
    -   the meter reading value is less than the current meter reading
    -   the meter type is different than the current meter type
-   Update Meter Average is ignored when:
    -   Meter Type = ECM
    -   No previous meter reading exists for the Unit
-   The Meter Reading API requests require a property called “Unit Identifier” that will contain one or more properties that will be used to identify the Unit to which the Meter Reading update applies.
-   The table below contains the possible valid Identifiers for the Meter Reading API.
    -   If the API cannot find a corresponding Unit and Unit Inventory record, an exception is thrown and the update request is not processed, marked with a 400 Bad Request status.
    -   If the provided Unit Identifier cannot be resolved to an individual record, the request will be rejected.

---

#### Identifiers

| Name | DataType | Comments |
|---|---|---|
| UnitID             | string | This is the unique database id for the Unit, the API will find the currently active Unit Inventory record for the specified Unit.  For Fusion, the API expects this string to contain an integer and will throw an Exception if it contains a non-Integer value.|
| UnitInventoryID    | string | This is the unique database id for the Unit Inventory, the API will find the corresponding Unit record for the specified Unit Inventory.  For Fusion, the API expects this string to contain an integer and will throw an Exception if it contains a non-Integer value.                                                            |
| UnitNumber         | string | This is used in conjunction with the "CustomerKey" and "CustomerBranchCode" fields, the API will use these three fields to locate the matching Unit Inventory record and then the corresponding Unit record.  This field cannot be used by itself, it can only be used in conjunction with "CustomerKey" and "CustomerBranchCode". |
| CustomerKey        | string | This is used in conjunction with the "UnitNumber" and "CustomerBranchCode" fields, the API will use these three fields to locate the matching Unit Inventory record and then the corresponding Unit record.  This field cannot be used by itself, it can only be used in conjunction with "UnitNumber" and "CustomerBranchCode".   |
| CustomerBranchCode | string | This is used in conjunction with the "CustomerKey" and "UnitNumber" fields, the API will use these three fields to locate the matching Unit Inventory record and then the corresponding Unit record.  This field cannot be used by itself, it can only be used in conjunction with "CustomerKey" and "UnitNumber".                 |
| VIN                | string | The Unit’s Vehicle Identification Number.|

 
### Request Properties

After a valid Identifier has been passed, the following Meter properties can be updated on the specified Unit/Unit Inventory record.

| Data Type | Definition | Validation Rules/Comments |
|----------------------|-------------|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Meter Type           | varchar(50) | Unit’s meter type                                            | Valid options are: Gallons, Hours, Kilometers, Liters, Miles, None, Billing, Other; will remain unchanged if Meter Type is not passed; Billing is used for LR Billing entries if configured in Fusion |
| Meter Reading        | decimal     | New meter reading of the Unit                                | Will remain unchanged if Meter Reading is not passed                                                                                  |
| Meter Reading Date   | datetime    | Date meter reading was updated                               | Will default to current date if not passed                                                                                            |
| Update Meter Average | bit         | When TRUE, the current meter average per day will be updated |   |
| ECM Reading          | decimal     | New ECM reading of the Unit                                  | Will remain unchanged if Meter Reading is not passed                                                                                  |
| ECM Reading Date     | datetime    | Date ECM reading was updated                                 | Will default to current date if not passed                                                                                            |
| VIN                  | varchar(20) | Vehicle Identification Number of the Unit.                   |   |


---

---

### Request

#### PUT request using UnitID as Unit Identidifier
```json
[
	{
		"Identifier":
		{
			"UnitId": "9448"
		},
		"MeterType" : "Miles",
		"MeterReading" : "25",
		"MeterReadingDate": "2019-12-10T14:09:00Z",
		"UpdateAvg" : "false"
	}
]
```



#### PUT request using VIN as Unit Identifier

```json
[
	{
		"Identifier":
		{
		"VIN" : "1GB6G2A66A1103234"
		},
		"MeterType" : "Miles",
		"MeterReading" : "250",
		"MeterReadingDate": "2019-1-14T14:09:00Z",
		"UpdateAvg" : "false"
	}
]
```



#### PUT request using CustomerKey/CustomerBranchCode/UnitNumber combination as Unit Identifier
```json
[
	{
		"Identifier":
		{
			"CustomerKey": "95082",
			"CustomerBranchCode": "01",
			"UnitNumber": "BX2045"
		},
		"MeterType" : "Miles",
		"MeterReading" : "250",
		"MeterReadingDate": "2019-1-14T14:09:00Z",
		"UpdateAvg" : "false"
	}
]
```



#### PUT request using UnitInventoryID as Unit Identifier
```json
[
	{
	"Identifier":
	{
		"UnitInventoryId" : "1852"
	},
	"MeterType" : "Miles",
	"MeterReading" : "250",
	"MeterReadingDate": "2019-1-14T14:09:00Z",
	"UpdateAvg" : "false"
	}
]
```

```json
{
    "UnitID" : "1852",
    "VIN" : "1GB6G2A66A1103234"
	"Status" : "Success",
	"Message" : null
}
}
```
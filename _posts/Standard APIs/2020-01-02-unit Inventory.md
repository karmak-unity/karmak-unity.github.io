---
layout: post
title: "Unit Inventory"
category: "Inventory" 
icon: "icon-truck"
type: "api" 
comments: false
description:   Allows users to update the inventory units within Fusion
---

---
The Unit API currently supports the PUT method to update existing Units in Fusion

**requires FUSION v3.59.0.0 or higher**

### PUT Method
To update a single unit:
```
https://api.karmak.io/api/unity/{version}/unityapi/unitinventory/unit
```
To update multiple units:
```
https://api.karmak.io/api/unity/{version}/unityapi/unitinventory/units
```

#### Usage and Limitations
-   The Unit API will allow updates to both the Unit record and the Unit Inventory record.
-   Requests require a property called “Identifier” that will contain one or more properties that will be used to identify the unit being updated. The API will attempt to resolve the identifier field(s) in a particular precedence and attempts to use the first one found. See hierarchy below:
    -   UnitInventoryID, else
        -   UnitID, else
            -   CustomerKey
            -   CustomerBranchCode
            -   Unit Number
-   Last Update Date will be updated to the current date/time.
-   Lase Update User will be updated to the Fusion User obtained from the Authorization token passed in with the API call.

**IDENTIFIER**

-   The table below contains the possible valid Identifiers for the Unit API..
    -   If the API cannot find a corresponding Unit and Unit Inventory record, an exception is thrown and the update request is not processed, marked with a 400 Bad Request status.

| Identifier | DataType | Comments |
|---|---|---|
| UnitID             | string | This is the unique database id for the Unit, the API will find the currently active Unit Inventory record for the specified Unit.  For Fusion, the API expects this string to contain an integer and will throw an Exception if it contains a non-Integer value.                                                                   |
|--------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UnitInventoryID    | string | This is the unique database id for the Unit Inventory, the API will find the corresponding Unit record for the specified Unit Inventory.  For Fusion, the API expects this string to contain an integer and will throw an Exception if it contains a non-Integer value.                                                            |
| UnitNumber         | string | This is used in conjunction with the "CustomerKey" and "CustomerBranchCode" fields, the API will use these three fields to locate the matching Unit Inventory record and then the corresponding Unit record.  This field cannot be used by itself, it can only be used in conjunction with "CustomerKey" and "CustomerBranchCode". |
| CustomerKey        | string | This is used in conjunction with the "UnitNumber" and "CustomerBranchCode" fields, the API will use these three fields to locate the matching Unit Inventory record and then the corresponding Unit record.  This field cannot be used by itself, it can only be used in conjunction with "UnitNumber" and "CustomerBranchCode".   |
| CustomerBranchCode | string | This is used in conjunction with the "CustomerKey" and "UnitNumber" fields, the API will use these three fields to locate the matching Unit Inventory record and then the corresponding Unit record.  This field cannot be used by itself, it can only be used in conjunction with "CustomerKey" and "UnitNumber".                 |

---
---

**REQUEST PROPERTIES**

After a valid Identifier has been passed, the following properties can be updated on the specified Unit/Unit Inventory Record.

|Name|DataType|Validation Rules/Comments|
|-----------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VIN                   | string  | If there is a length specified for the Unit's Manufacturer then the API will ensure the updated value conforms to that length.  If the Manufacturer is also being updated in this request, then the VIN length requirement from the new Manufacturer is used.  If the Unit already has a non-blank VIN present then an Exception is thrown and the update request is not completed.  VIN cannot be null. |
| ProductionYear        | integer | ProductionYear must be a valid year component of a DateTime variable; must be a 4 digit number between 1753 and 9999.                                                                                                                                                                                                                                                                                    |
| Model                 | string  | The API will verify that the Manufacturer/Make/Model combination is valid before applying the update.  If Make and/or Manufacturer is also being updated then those values are used when performing this check.                                                                                                                                                                                          |
| Make                  | string  | The API will verify that the Manufacturer/Make/Model combination is valid before applying the update.  If Model and/or Manufacturer is also being updated then those values are used when performing this check.                                                                                                                                                                                         |
| Manufacturer          | string  | The API will verify that the Manufacturer/Make/Model combination is valid before applying the update.  If Make and/or Manufacturer is also being updated then those values are used when performing this check.                                                                                                                                                                                          |
| MeterType             | string  | The API will lookup the MeterType and if found it will apply the update, if not an Exception is thrown and the update request is not completed.                                                                                                                                                                                                                                                          |
| LotLocation           | string  | This is used in conjunction with LotLocationBranchCode, the API will ensure that a valid LotLocation can be found using both properties and if found it will apply the update, if not an Exception is thrown and the update request is not completed.                                                                                                                                                    |
| LotLocationBranchCode | string  | This is used in conjunction with LotLocation, the API will ensure that a valid LotLocation can be found using both properties and if found it will apply the update, if not an Exception is thrown and the update request is not completed.                                                                                                                                                              |
| CharacteristicType    | string  | The API will lookup the CharacteristicType and if found it will apply the update, if not an Exception is thrown and the update request is not completed.                                                                                                                                                                                                                                                 |
| PurchaseCost          | decimal | The API will ensure the value is greater than or equal to zero and if so it will apply the update, if not an Exception is thrown and the update request is not completed.                                                                                                                                                                                                                                |
| ActualCashValue       | decimal | The API will ensure the value is greater than or equal to zero and if so it will apply the update, if not an Exception is thrown and the update request is not completed.                                                                                                                                                                                                                                |
| UnitType              | string  | The API will lookup the UnitType and if found it will apply the update, if not an Exception is thrown and the update request is not completed.                                                                                                                                                                                                                                                           |

 **RESPONSE PROPERTIES**

The response will include the Identifier information specified in the request, as well as a Status field and a message to indicate the outcome of the update request.

|Name|DataType| DEscription |
|---|---|---|
|CustomerKey|string| This is the Fusion Customer Number |
|CustomerBranchCode|string| This is the branch of the customer  |
|UnitNumber|string| This is used in conjunction with the "CustomerKey" and "CustomerBranchCode" fields |
|UnitID|string|   This is the unique database id for the Unit |
|UnitInventoryID|string| This is the unique database id for the Unit Inventory, the API will find the corresponding Unit record for the specified Unit Inventory.  |
|Status|string| |
|Message|string| ||

---
---

### Sample PUT Request (Single Unit)
```json	
{
	"Identifier":
	{
		"UnitId": "19052"
	},
	"Vin": "1122180419",
	"ProductionYear": "2020",
	"Model": "Edge",
	"Make":"Ford",
	"Manufacturer":"Ford",
	"MeterType":"Miles",
	"LotLocation": "East Side",
	"LotLocationBranchCode": "01",
	"CharacteristicType":"White Truck",
	"PurchaseCost":"2.00",
	"ActualCashValue":"10.00",
	"UnitType":"SUV"
}
```

### Response Code (200 OK) (Single Unit)
```json
{
	"CustomerKey": null,
	"CustomerBranchCode": null,
	"UnitNumber": null,
	"UnitId": "19052",
	"UnitInventoryId": null,
	"Status": "Success",
	"Message": "All good here"
}
```

---
---
### Sample PUT Request (Single Unit - Specific Fields)
```json	
[
	{
		"Identifier":
		{
			"UnitID": "9422"
		},
		"LotLocation": "East",
		"LotLocationBranchCode": "01"
	}
]
```

### Response Code (200 OK) (Single Unit)
```json
[
	{
		"CustomerKey": null,
		"CustomerBranchCode": null,
		"UnitNumber": null,
		"UnitID": "9422",
		"UnitInventoryID": null,
		"Status": "Success"
		"Message": "All good here"
	}
]
```
---
---

### Sample PUT Request (Multiple Units)
```json	
[
	{
		"Identifier":
		{
			"UnitId": "19052"
		},
		"Vin": "1122180419",
		"ProductionYear": "2020",
		"Model": "Edge",
		"Make":"Ford",
		"Manufacturer":"Ford",
		"MeterType":"Miles",
		"LotLocation": "East Side",
		"LotLocationBranchCode": "01",
		"CharacteristicType":"White Truck",
		"PurchaseCost":"2.00",
		"ActualCashValue":"10.00",
		"UnitType":"SUV"
	},
	{
		"Identifier":
		{
			"UnitId": "19072"
		},
		"Vin": "1122180420",
		"ProductionYear": "2020",
		"Model": "Edge",
		"Make":"Ford",
		"Manufacturer":"Ford",
		"MeterType":"Miles",
		"LotLocation": "West Side",
		"LotLocationBranchCode": "01",
		"CharacteristicType":"White Truck",
		"PurchaseCost":"2.00",
		"ActualCashValue":"20.00",
		"UnitType":"SUV"
	}
]
```

### Response Code (200 OK) (Multiple Units)
```json
[
    {
		"CustomerKey": null,
		"CustomerBranchCode": null,
		"UnitNumber": null,
		"UnitId": "19052",
		"UnitInventoryId": null,
		"Status": "Success",
		"Message": "All good here"
    },
	{
		"CustomerKey": null,
		"CustomerBranchCode": null,
		"UnitNumber": null,
		"UnitId": "19072",
		"UnitInventoryId": null,
		"Status": "Success",
		"Message": "All good here"
    }
]
```

---
---
### Sample PUT Request (Multiple Units - Specific Fields)
```json	
[
	{
		"Identifier":
		{
			"UnitId": "9422"
		},
		"LotLocation": "East",
		"LotLocationBranchCode": "01"
	},
	{
		"Identifier":
		{
			"UnitId": "9433"
		},
		"LotLocation": "West",
		"LotLocationBranchCode": "01"
	}
]
```

### Response Code (200 OK) (Multiple Units)
```json
[
	{
		"CustomerKey": null,
		"CustomerBranchCode": null,
		"UnitNumber": null,
		"UnitId": "9422",
		"UnitInventoryId": null,
		"Status": "Success",
		"Message": "All good here"
	},
	{
		"CustomerKey": null,
		"CustomerBranchCode": null,
		"UnitNumber": null,
		"UnitId": "9433",
		"UnitInventoryId": null,
		"Status": "Success",
		"Message": "All good here"
	}
]
```

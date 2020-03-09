---
layout: post
title: "Unit Characteristics"
category: "Inventory" 
icon: "icon-truck"
type: "api" 
comments: false
description:   Allows users to update Unit Characteristics values on active units in Fusion
---

The Unit Characteristics API will be used to update Unit Characteristics values on active units in Fusion.

> **requires FUSION v3.59.0.0 or higher.**


### POST Method
The Unit Characteristics API supports the POST method to update Unit Characteristics values in Fusion.
```
http://api.karmak.io/api/unity/{version}/unityapi/unit/characteristics
```

### Unit Identifier Resolution Model
```json
{
	"CustomerKey": "95082",
	"CustomerBranchCode": "01",
	"UnitNumber": "BX2045",
	"UnitId": "9788",
	"UnitInventoryId": "22490"
}
```
#### JSON API MAP


|Field|Description|Possible Values|
|---|---|---|
|Unit Identity|Allows the request to reference the Unit in 1 of 3 ways, and the resolver processes the model to validate the Unit. (Hierarchy and rules for Unit identifiers described in Rules section below.)|<b>Customer Key</b><BR>Unit’s owning customer number; must be used with Customer Branch Code and Unit Number<BR><b>Customer Branch Code</b><BR>Branch Code of Unit owning Customer; must be used with Customer Key and Unit Number<BR><b>Unit Number</b><br>Number assigned to specified Unit; must be used with Customer Branch Code and Customer Key<BR><b>Unit ID</b><br>Unique database ID for the specified Unit record<BR><b>Unit Inventory ID</b><br>Unit database ID for the specified Unit Inventory record |
|Characteristic Identity|Allows the request to reference the Characteristic in 1 of 2 ways, and the resolver processes the model to validate the Unit. (Rules for Characteristic identifiers described in Rules section below.)|<b>ID</b><BR>the database ID for the Characteristic being passed<BR><b>Characteristic</b><br>the Characteristic Name for the Characteristic being passed.|
|Value|The value used to update the specified characteristic prompt. (Rules for values described in Rules section below.)|The value must meet the data type requirements of the characteristic as set in the miscellaneous prompt in Fusion.|


#### Rules for Unit Identifier Resolution

Requests require a property called “UnitIdentifier” that will contain one or more properties that will be used to identify the unit being updated. The API will attempt to resolve the identifier field(s) in a particular precedence and attempts to use the first one found. See hierarchy below:
-   UnitInventoryID, else
	-   UnitID, else
		-   CustomerKey
		-   CustomerBranchCode
		-   Unit Number

When UnitInventoryID is passed, it will be used to resolve the Unit.
-   If an invalid UnitInventoryID is passed, the response will be
	-   Status: 'ERR'
	-   Message: ‘No matching Unit could be found using UnitInventoryID = {UnitInventoryID}.’

When UnitID is passed, it will be used to resolve the Unit.
-   The API first looks for an active occurrence for the UnitID.
-   If an invalid UnitID is passed, the response will be
	-   Status: 'ERR'
	-   Message: ‘No matching Unit could be found using UnitID = {UnitID}.’

If not using UnitInventoryID or UnitID, then CustomerKey, CustomerBranchCode, and UnitNumber must all be passed in the request.
    -   The branch code and customers are both validated, and a unit inventory lookup is performed.
    -   If a Unit cannot be found using the CustomerKey, CustomerBranchCode, UnitNUmber combination, the response will be
        -   Status: 'ERR'
        -   Message: ‘No matching Unit could be found using UnitNumber = {UnitNumber} and CustomerKey = {Customer Key} and CustomerBranchCode = {CustomerBranchCode}.’


---
---

### Unit Characteristics Resolution Model
```json
{
	"Id": "75",
	"Characteristic": "Interior Color"
}
```

---

#### Rules for Unit Characteristics Resolution

The request must include a characteristic identifier for resolution. The
characteristic identifier can be either the Characteristic Name or the
Characteristic ID. See hierarchy below.

-   Characteristic ID, else
    -   Characteristic Name
-   When a Characteristic ID cannot be resolved, the response will be
    -   Status: ‘ERR’
    -   Message: ‘Could not resolve the misc prompt with ID {id}.’
-   When a Characteristic Name cannot be resolved, the response will be
    -   Status: ‘ERR’
    -   Message: ‘Could not resolve the misc prompt {Characteristic Name}.’

---

#### Setting the Unit Characteristic

The datatype of the miscellaneous prompt is used to validate the value passed to
update the Unit Characteristic.

Validation will fail (Status = 'ERR') in the following scenarios:

-	a request is made to ‘blank’ a required misc prompt
	-   Message: ‘{Characteristic Name} is required and must have a value.’

-   a request is made to update a single character value to a value longer than a single character
    -   Message: ‘Value for {Characteristic Name} must be a single character.’

-   a request is made to update a value longer than the 50 character maximum
    -   Message: ‘Value for {Characteristic Name} must be a maximum of 50 characters.’

-   a request is made to update a value to an invalid Date
    -   Message: ‘Value for {Characteristic Name} must be a valid date/time.’

-   a request is made to a update a value it an invalid decimal value
    -   Message: ‘Value for {Characteristic Name} must be a valid number with a max of 6 positions after the decimal point.’

-   a request is made to update the value to an invalid monetary/dollar value, no dollar sign allowed
    -   Message: ‘Value for {Characteristic Name} must be a valid number with a max of 2 positions after the decimal point.’

-   If a value passed in the request is otherwise valid for the datatype, but there is Validation List associated with the miscellaneous prompt and the incoming value is not in the list
    -   Message: ‘{Value} is not a valid value for prompt {Characteristic
        Name}.’

---
---

## REQUEST/RESPONSE EXAMPLES


### REQUEST

A PUT request to using the following identifiers
-   Unit Identifier = Unit Inventory ID
-   Characteristic Identifier = Characteristic

```json
[
	{
		"unitIdentity":
		{
			"unitInventoryId" : "22490"
		},
		"characteristicIdentity":
		{
			"characteristic": "Interior Color"
		},
		"value": "Brown"
	}
]
```

### RESPONSE

```json
[
	{
		"UnitIdentifier": 
		{
			"CustomerKey": "95082",
			"CustomerBranchCode": "01",
			"UnitNumber": "BX2045",
			"UnitId": "9788",
			"UnitInventoryId": "22490"
		},
		"CharacteristicIdentity":
		{
			"Id": "75",
			"Characteristic": "Interior Color"
		},
		"Status": "Success",
		"Message": null
	}
]
```

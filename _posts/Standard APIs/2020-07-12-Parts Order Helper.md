---
layout: post  
title: "Parts Order Helpers"  
category: "Parts Sales Order"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: Helper APIs for Creating Parts Order, Get Avaialble Payments and Pickup / Delivery Methods 
---

The Part Search Helper APIs provide information and details to successfully submit a parts order

***NOTE: Requires Fusion version 3.60.10***

---
---


### Available Payment Methods
-------------------------

Provides a list of available payment methods to submit with a Parts Sales Order.

1 submitted field: “customerID”

#### Fields

| Field Name  | Size | Description                                                              |
|-------------|------|--------------------------------------------------------------------------|
| ID          |      | ID Associated with the Payment Method                                    |
| Method      | 30   | Payment Method must match a payment method setup on the business system. |
| Description |      |                                                                          |


#### REQUEST POST URL
```
.../unityapi/AvailablePaymentMethods
```
 

#### Sample Request
```json
{
	"customerID": "8827892",
	"locationID": "1"
}
```
 

#### Sample Response
```json
[
	{
		"ID": "01",
		"Method": "Credit Card",
		"Description": ""
	},
	{
		"ID": "02",
		"Method": "Store Credit"
		"Description": ""
	},
	{
		"ID": "03",
		"Method": "C.O.D."
		"Description": ""
	},
]
```
 
-------------------------


### Pickup / Delivery Methods
-------------------------

Provides a list of available valid pick up and delivery methods by Branch location to submit with a Parts Sales Order.


POST endpoint to look up and return a list of the delivery methods for parts by branchID

| Field | Field Type | Description |
|----|--------|----------------------------------------------|
| ID | String | This is the Branch ID that will be looked up |


---

#### REQUEST POST URL
```
.../unityapi/PickupDelivery
```

#### Sample Request
```json
[
	{
		"branchID": "1234"
	}
]
```
 

#### Sample Response
```json
[
	{
		"criteria": {
			"branchID": "1234"
		},
	"deliveryMethods": [
		{
			"deliveryMethod": "PickUp"
		},
		{
			"deliveryMethod": "Delivery to Shop"
		},
		{
			"deliveryMethod": "Pick Up main Branch"
		},
		{
			"deliveryMethod": "Delivery to Remote"
		},
	]

	}
]
```


-------------------------


### Department Lookup
-------------------------


This is the GET Endpoint to look up and return a list of the Department IDs by Branch(Location) ID.

| Field | Field Type | Description |
|----|--------|----------------------------------------------|
| BranchID | Integer | The id of the location you’d like to find departments for.|


---


#### REQUEST POST URL
```
.../unityapi/Departments?BranchID=x
```
 

#### RESPONSE
```json
{
    "Departments": [
        {
            "Name": "Admin",
            "Type": "Accounting",
            "ID": 0
        },
        {
            "Name": "Body Shop",
            "Type": "Service",
            "ID": 0
        },
        {
            "Name": "Bus",
            "Type": "Sales",
            "ID": 0
        },
        {
            "Name": "Equipment",
            "Type": "Parts",
            "ID": 0
        },
    ],
    "Messages": [
        "Success!"
    ]
}
```
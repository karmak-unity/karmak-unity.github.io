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

When submitting a Parts Order, I need to be able to look up the Available Payment Methods for the customer so I can submit my parts order correctly.

1 submitted field: “customerID”

#### Fields

| Field Name  | Size | Description                                                              |
|-------------|------|--------------------------------------------------------------------------|
| ID          |      | ID Associated with the Payment Method                                    |
| Method      | 30   | Payment Method must match a payment method setup on the business system. |
| Description |      |                                                                          |

#### Sample Request
```json
{
	"customerID": "8827892"
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

When creating a parts order, I need to know which are valid pick up and delivery methods by Branch location.

GET endpoint to look up and return a list of the delivery methods for parts by branchID

| Field | Field Type | Description |
|----|--------|----------------------------------------------|
| ID | String | This is the Branch ID that will be looked up |


---


#### Sample Request
```json
[
	{
		"ID": "1234"
	}
]
```
 

#### Sample Response
```json
[
	{
		"criteria": {
			"ID": "1234"
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
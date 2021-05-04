---
layout: post   
title: "GET Available Suppliers"  
category: "System"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: Allow user to get available Parts suppliers in Fusion.
---

When submitting a Parts Purchase Order, a user needs to be able to look up the Suppliers in Fusion for the Company so as user can submit their parts purchase
order correctly.

* Suppliers in Fusion are setup Company Wide
* The Token will be passed in on the GET to identify the Fusion Client who’s Suppliers will be returned in the response.
* Only Active Suppliers will be returned.

***NOTE: Requires Fusion version 3.61.5***


#### Response Fields

| ID          |     | Unique ID of the Supplier from the Fusion database. |
|-------------|-----|-----------------------------------------------------|
| Supplier    | 20  | Supplier Code                                       |
| CompanyName | 100 | Company Name of the Supplier                        |

### GET
```
/api/unity/{version}/unityapi/AvailableSuppliers
```
 

### SAMPLE RESPONSE
```
[
	{
		"ID": "01",
		"Supplier": "Napa",
		"CompanyName": "Napa of Carlinville"
	},
	{
		"ID": "02",
		"Supplier": "Stemco",
		"CompanyName": "Stemco Products"
	},
	{
		"ID": "03",
		"Supplier": "FG",
		"CompanyName": "Fleetguard"
	}
]
```
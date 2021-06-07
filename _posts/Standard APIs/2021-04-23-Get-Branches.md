---
layout: post   
title: "GET Available Branches"  
category: "System"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: Allow user to get available Branches in Fusion.
---


When submitting a Parts Parts Order, a user needs to be able to look up the Branches for the Company so I can submit my parts purchase order correctly.

* Branches in Fusion are setup Company Wide
* The Token will be passed in on the GET to identify the Fusion Client who’s Branches will be returned in the response.
* Only Active Branches will be returned.

**Requires Updated Fusion Version: 3.62.00 or newer**

#### Response Fields

| Field Name | Size |			Description		|
|-----------------|-----|--------------------------------------------------------------------------------|
| ID                   |     | Unique ID associated with the Branch from the Fusion database                                         |
| BranchCode           | 10  | Branch Code                                                                                           |
| BranchName           | 100 | Branch Name                                                                                           |
| CustomerBaseBranchID | 10  | Unique ID of the Fusion Branch that is identified as the Customer Base Branch of the returned Branch. |


### Sample GET Request
```
/api/unity/{version}/unityapi/Branch
```

### Sample Response:
```json
[
	{
		"ID": "1",
		"BranchCode": "CAR",
		"BranchName": "Karmak of Carlinville",
		"CustomerBaseBranchID": "1"
	},
	{
		"ID": "2",
		"BranchCode": "SPG",
		"BranchName": "Karmak of Springfield",
		"CustomerBaseBranchID": "1"
	},
	{
		"ID": "3",
		"BranchCode": "SPF",
		"BranchName": "Karmak of Spanish Fort",
		"CustomerBaseBranchID": "3"
	}
]
```
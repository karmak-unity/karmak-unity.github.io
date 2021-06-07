---
layout: post   
title: "GET Available AP Vendors"  
category: "System"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: Allow user to get available AP Vendors in Fusion.
---

This provides a look up the AP Vendors for the Company so I can submit information correctly.

Notes:
* AP Vendors in Fusion are setup Company Wide
* The Token will be passed in on the GET to identify the Fusion Client who’s AP Vendors will be returned in the response.
* Only Active AP Vendors will be returned.

**Requires Updated Fusion Version: 3.62.00 or newer**

#### Response Fields

| Field Name | Size |			Description		|
|-----------------|-----|--------------------------------------------------------------------------------|

| ID              |     | Unique ID associated with the AP Vendor from the Fusion database               |
| APVendor        | 10  | AP Vendor                                                                      |
| CompanyName     | 100 | Company Name of the AP Vendor                                                  |
| ControlBranchID |     | Unique Branch ID of the Control Branch of the Control Branch of the AP Vendor. |


### GET
```
/api/unity/{version}/unityapi/APVendor
```

###Response:

```json
[
  {
    "ID": "01",
    "APVendor": "012367",
    "CompanyName": "Napa of Carlinville",
    "ControlBranch": "02"
  },
  {
    "ID": "02",
    "APVendor": "12332"
    "CompanyName": "Cintas",
    "ControlBranch": ""
  },
  {
    "ID": "03",
    "APVendor": "22112"
    "CompanyName": "Napa Corporate",
    "ControlBranch": ""
  },
]
```
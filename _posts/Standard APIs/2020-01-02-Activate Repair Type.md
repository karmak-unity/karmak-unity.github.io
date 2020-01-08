---
layout: post
title: "Activate Repair Type"
category: "Service" 
icon: "icon-wrench"
type: "api" 
comments: false
description:  supports a single request to update the repair type to active
---

---
The PUT method will be used to update a single repair type to active


### PUT Method
```
https://api.karmak.io/api/unity/{version}/unityapi/RepairType/UpdateRepairType
```


*    The following fields are required when passing in a PUT request:
	*	Repair Group
		* Must be a valid Fusion Repair Group.
    *    Repair Type
        *    Must be valid Fusion Repair Type
    *   Active 
        *    A boolean field that will set or update the Inactive flag on the Repair Type.
        *   Set to TRUE to set the Repair Type to Active in Fusion
        *    Set to FALSE to set the Repair Type to Inactive in Fusion

The Activate Repair Type API supports a single request/response method, and therefore only one Repair Type  flag can be set/updated at a time.  To update multiple Repair Types, multiple calls are required.

| JSON API Map | Description                                                                       | Data Type        |Required   |
|---------------|------------------------------------------------------------------------|---------|---|
| “RepairGroup” | The Repair Group of the Repair Type to be updated.                     | string  | Y |
| “RepairType”  | The Repair Type to be updated - must be within the above Repair Group. | string  | Y |
| “Active”      | Used to set the Repair Type to Active or Inactive in Fusion.           | boolean | Y |

---
---

### Sample PUT Request
```json	
{
	"RepairGroup" : "006",
	"RepairType" : "000",
	"Active" : "false"
}
```

### Response Code (200 OK)
```json
{
	"RepairGroup" : "006"
	"RepairType" : "000"
	"Status" : "Success"
	"Message" : ""
}
```
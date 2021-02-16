---
layout: post
title: "Create and Update Technicians"  
category: "Service"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: Allow user to create and update Technicians in Fusion.
---

The Technicians API allows users to Create and Update Technician records in Fusion

## Overview

The Technicians API in Karmak Unity will allow 3rd Parties to Create, Update and Get information about Technicians setup in the Fusion Business System.  In order to create a Technician, a valid Fusion user must be setup which can be done via the Fusion Business System or using the  API in Karmak Unity.

### POST
```
https://api.karmak.io/api/unity/{version}/unityapi/user/CreateTechnician
```

### PUT
```
https://api.karmak.io/api/unity/{version}/unityapi/user/UpdateTechnician
```

### GET

Use the below link to access the Unity documentation to perform a GET on the Techncian Data Access Object to get information about Fusion Technicians

https://unity.karmak.io/Technician.html

### Specifications

#### POST

* The POST method will be used to create Technician Records in Fusion.

* Only one Technician record will be allowed in a single request call.

* The Technician Identity section will be ignored when creating a Technician

* This Base Branch, Base Department and Shift passed in will be used as the Base Work Location that is created for the Technician record when it is created.  

* If the Technician Number or User Name is found for an existing Technician record the record will not be created.  

* A response will be provided with a message section that will outline a success or any issues that prevented the Technician from being created.

* The Fusion Username used in the Unity API call will be used as the Add and Last Update User of the Technician created.

* The Date and Time the Unity API call was made will be used as the Add Date and Last Update of the Technician created.

* The Technician record will be created in Fusion following the standard create logic of the SVM94150 Technician form in Fusion outside of any specific rules listed in this section and the POST/PUT Request Fields Section below. 

#### PUT

* The PUT method will be used to update Technician Records in Fusion.

* Only one Technician record will be allowed in a single request call.

* Only fields that are expected to be updated should be passed in outside of the required fields.

* In order to update an existing Technician record the user will be required to send in the Technician in the Technician Identity section to find a match. If a match isn’t found an update will not be performed.

* A response will be provided with a message section that will outline a success or any issues that prevented the Technician from being updated.

* The Fusion Username used in the Unity API call will be used as the Last Update User of the Technician updated.

* The Date and Time the Unity API call was made will be used as the Last Update Date of the Technician updated.


### Request Fields

| Field               | Field Type | Required | Length | POST Business Rules and Defaults                                                                                                                            | PUT Business Rules and Defaults                                                                                                                             |
|---------------------|------------|----------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Technician Identity | Node       |    |  | This will be ignored in a POST                                                                                                                              | This section will be used to identify the Technician that will be updated.                                                                                  |
| TechnicianNumber    | integer    | Yes      | 20     | | This is the Technician that will be looked up in order to update information about the record.                                                              |
| Main Body           |      |    |  | | |
| TechnicianNumber    | integer    | Yes      | 20     | This is the Technician that will be created.                                                                                                                | This is the Technician Number value that will be updated to of the looked up record.                                                                        |
| UserName            | string     | Yes      | 20     | This is User Name that the Technician Number will be created for.  This must match a valid User Name setup in Fusion.                                       | This is the User Name value that will be updated of the looked up record.                                                                                   |
| Shift               | string     | Yes      |  | This is the Shift the Technician record will be created for.  This must match a valid Shift setup in Fusion.                                                | This is the value the Shift will be updated to on the looked up record.                                                                                     |
| Rate                | decimal    | Yes      |  | This is the Rate per hour of the Technician record being created.  This must be greater than 0.                                                             | This is the value the Rate per Hour of the looked up record will be updated to.  This must be greater than 0                                                |
| BaseBranch          | string     | Yes      | 10     | This is the Branch Code the Technician record will be created for.  This must match a valid Branch Code in Fusion                                           | This is the value the Branch of the looked up record will be updated to.  This must match a valid Branch Code in Fusion.                                    |
| BaseDepartment      | string     | Yes      | 10     | This is the Department the Technician record will be created for.  This must match a valid Department in Fusion                                             | This is the value the Department of the looked up record will be updated to.  This must match a valid Department in Fusion.                                 |
| HireDate            | Date       |    |  | This is the Hire Date of the Technician being created.  This will default to the Current Date if not passed in.                                             | This is the Hire Date of the looked up record will be updated to.                                                                                           |
| IsInactive          | bit        |    | 1      | This will set the Technician record to Inactive.  Set this to true to identify the Technician as Inactive otherwise the default will be assumed as false.   | This will set the Technician record to Inactive.  Set this to true to identify the Technician as Inactive otherwise the default will be assumed as false.   |



### POST Request
```json
{              
               "TechnicianNumber":"20003",
               "Username":"spool",
               "BaseBranch":"01",
               "BaseDepartment":"Service",
               "shift":"Day",
               "rate":25.00                 
                }
```

### POST Response
```json
{
    "Status": "Technician created successfully.",
    "Message": null
}
```

### PUT Request
```json
{
    "Identity": {
       "TechnicianNumber": "101"
        
    },
               "rate":"20.00"
                }
```

### PUT Response	
```json
{
    "Status": "Technician updated.",
    "Message": null
}
```
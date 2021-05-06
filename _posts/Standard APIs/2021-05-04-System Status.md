---
layout: post
title: "System Status"  
category: "System"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: Allow API Consumers to check and validate the status and version of the Fusion instance they are interating with.
---



## Overview
The System Status allows API Consumers to check and validate the status and version of the Fusion instance they are interating with.




### GET
```
https://api.karmak.io/api/unity/{version}/unityapi/System/System/Status
```


### Response Fields

| FIELD	 |  TYPE	 | 	DESCRIPTION | 
|---|---|---|
| IsOnline	 | boolean	 | 	Indicates the system is online and accessible |  
| BridgeVersion	 | string	 | Version of communication system |  
| FusionVersion	 | string	 | Version of Fusion system | 
| Account	  | string	 | Account resolved from request | 
| User	  | string	 | User resolved from request | 
| Message		 | string	 | Message associated with the status request | 



### GET Request and Response 
```
https://api.karmak.io/api/unity/{version}/unityapi/System/System/Status
```

```json
{
    "IsOnline": true,
    "BridgeVersion": "3.61.4.0",
    "FusionVersion": "3.61.4.0",
    "Account": "5079d18b-6cdf-4297-95cd-30785513ac93",
    "User": "867ec00f-ef78-431b-8814-647ff6137990",
    "Message": "Successfully sent message to Bridge",
    "ProcessGUID": "5358182b338c6744a946ed588c4e66e2"
}
```

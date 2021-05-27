---
layout: post
title: "System Response Codes"
category: "General Documentation"
type: "usage" 
comments: false
description: Common system response codes and Error messages.
---

<a name="200">&nbsp;</a>
### 200 - OK
**What does it mean?**

This request was successful, the body contains the requested data in JSON format.  If the body only contains a ProcessGUID, this means there was no data available that matched the request.


<a name="201">&nbsp;</a>
### 201 - Created
**What does it mean?**

201 indicates that the record was successfully created in the system. 

<a name="4xx">&nbsp;</a>
## 4xx  Response Codes

This class of status code is intended for situations in which the error seems to have been caused by the client. 

<a name="400">&nbsp;</a>
### 400 - Bad Request
**What does it mean?**

The 400 error means there was something incorrect within the API request. They are usually accompanied with a message.  This typically indicates an issue occurred with the security token/information provided on the request.  Either the token was missing, was invalid, or couldn't be matched to any known values, or the model submitted was invalid. 

#### "Invalid Model"
This indicates the body of your message was not formatted correctly. The most obvious is submitting an array versus an object. 

##### **Array**<BR>
An array contains one or more objects

```json
[
    {
        "Branch" : "01",
        "RepairOrder": 190657,
        "Task" : 1,
        "PartNumber": "2174733676",
        "Supplier" : "LAR",
        "Rounding" : "D",
        "OverridePrice": 19.99,
        "Quantity": "3.9"
    }     
]
```

##### **Object**<BR>
An object is a single set of data for a single record or action

```json
{
	"Branch" : "01",
	"RepairOrder": 190657,
	"Task" : 1,
	"PartNumber": "2174733676",
	"Supplier" : "LAR",
	"Rounding" : "D",
	"OverridePrice": 19.99,
	"Quantity": "3.9"
}     
```

<a name="401">&nbsp;</a>
### 401 - Unauthorized
**What does it mean?**

The error 401 occurs when you need to enter credentials (a username and password or an authorization token) to access the API. This can signify that your credentials are incorrect, or your authorization token has expired


<a name="403">&nbsp;</a>
### 403 - Forbidden

**What does it mean?**

The request contained valid data and was understood by the server, but the server is refusing action. This may be due to the user not having the necessary permissions for a resource or needing an account of some sort, or attempting a prohibited action (e.g. creating a duplicate record where only one is allowed).  The request should not be repeated.


<a name="404">&nbsp;</a>
### 404 - Not Found
**What does it mean?**

This indicates the API URL you attempted to access does not exist. Please check the URL of your API call. 

<a name="405">&nbsp;</a>
### 405 - Method Not Allowed
**What does it mean?**

405 indicates an improper method was called. example: POST sent when the endpoint only accepts GET. please check the documentation and review your API method. 


<a name="408">&nbsp;</a>
### 408 - Request Timeout 

**What does it mean?**

The 408 Request Timeout Error code occurs when a connection with the website is timed out. It means the request you made to the web server is taking too much time as compared to the waiting time of the website's server. Client requests load time is much higher than the server's waiting time for a particular request.

In the instances where this error is returned by the API platform (from Fusion). It indicates that the Fusion system timed out while trying to perform the request


<a name="415">&nbsp;</a>
### 415 - Unsupported Media Type
**What does it mean?**

This indicates that the server refuses to accept the request because the payload format is in an unsupported format. The format problem might be due to the request's indicated Content-Type or Content-Encoding , or as a result of inspecting the data directly. 

<a name="429">&nbsp;</a>
### 429 - Too Many Requests
**What does it mean?**

429 indicates you have exceeded a quota or rate limit. You will need to pause sending requests until the system has cleared your quote or rate threshold. Please validate the rate at which you are sending queries. If you find, you need increased limits, please contact Unity Business Sales to increase your limit. (Fees may apply) 

<a name="500">&nbsp;</a>
### 500 - Internal Server Error
**What does it mean?**

This is a server-side error, (for Karmak.io, it is an error response from Fusion DMS).

<a name="502">&nbsp;</a>
### 502 - Bad Gateway
**What does it mean?**

502 indicates that karmak API server has gotten a bad response from that other server (Fusion Instance).

<a name="504">&nbsp;</a>
### 504 - Gateway Timeout
**What does it mean?**

504 indicates Karmak.io did not receive a timely response from the Fusion instance.

<a name="515">&nbsp;</a>
### 515 - SQL Server Error
**What does it mean?**

An example of a 515 can occur at execution time when a field has a NOT NULL default and you try to insert a NULL value into that column.

---
layout: post
title: "Using Unity"
category: "General Documentation"
type: "usage" comments: false
description: Details the process by which a user can request an access token, recieve a bearer token, and a Unity API call is sent to the sytem.
---

Karmak's Unity platform provides a standard set of APIs, which can be used by customers to access their own data, or for integration with approved third parties.  This document details the process by which a Unity API call is made.

## Obtaining a Bearer Token

Before making any calls to Unity API's, you must first obtain a Bearer Token,
which must be passed on each API request.

Unity uses OAuth 2.0 compatible access control, closely resembling the standard
"client_credentials" flow (grant type), with some additional information
required. 

Bearer Tokens (access tokens) are obtained using a properly formatted HTTPS
request, as detailed here:

<BR>
---

### HTTPS METHOD
POST

<BR>
---

### URL
#### QA
```
https://qa.karmak.io/auth/connect/token
```
Not all customers have QA environments deployed - use only if instructed by Karmak Support

<BR>
#### Production
```
https://api.karmak.io/auth/connect/token
```

<BR>
---

| **Headers**                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                                                                                     |
|---|---|---|
| **Header**                  | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | **Value**                                                                                                           |
| Content-Type                | Must be URL-encoded in standard x-www-form-urlencoded format                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | application/x-www-form-urlencoded                                                                                   |

<BR>
---

| **Body**                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                                                                                     |
|---|---|---|
| **Parameter**               | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | **Value**                                                                                                           |
| Client_ID                   | Unique Partner Identifier                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | *Please contact Karmak Partner Support for Client_ID; see Client_ID Notes below.*                                   |
| Client_Secret               | Partner Password                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | *Please contact Karmak Partner Support for Client_Secret*                                                           |
| Grant_Type                  | Must be exact value:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | karmak_identity                                                                                                     |
| Scope                       | Must be exact value:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | api                                                                                                                 |
| Account                     | ID representing the Karmak customer account being accessed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | *Please contact Karmak Partner Support for Account ID*                                                              |
| User                        | User ID for the account being accessed; ties to a Fusion user                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | *Provided by Karmak Partner Support; see User notes below.*                                                         |

<BR>
---

## NOTES
### Client_ID

The Client_ID (and associated Client_Secret) are issued by Karmak Support to customers or partners authorized to access Unity.  The Client_ID uniquely identifies the partner or customer to which it is issued.

Partners use their Client_ID to authenticate, and specify using the Account and User parameters which customer to access.

Customers accessing their own data will be issued their own Client_ID.  The Account and User parameters are still required.

Client_ID's are only to be used by the party to whom they are issued.  Customers are not to provide Client_ID's issued to them to any third party without prior approval by Karmak. 

**If an additional separate Client_ID is needed for any reason, please contact Karmak Support.**                                                                                                                                                                                      
### User
The User ID referenced is within our Unity systems, and is not the same as a Fusion Username.  However, a Fusion username may be linked to a User ID - this step is necessary in order to access Fusion as the Fusion username.   As a part of initial setup Karmak Partner Support will: 
- Create a new Fusion service username within the customer's Fusion system that represents the Partner or customer Unity access.
- Create a Unity User that is associated with this Fusion service username.
- Provide the Unity User ID to the Partner or customer.

If the partner provides services to multiple Karmak customers, the above process will be completed for each customer Account.
Multiple Users 
-     A Client_ID can access multiple Account/User combinations (i.e., one Partner can make API requests to multiple Karmak customer Accounts).
	- A separate token must be obtained for each Account/User combination needed.
- A single Account can support multiple Users for the Account
	- At the User level, there is a 1:1 relationship with Fusion usernames (i.e., one User can only be associated with one Fusion username)

Please contact Karmak Partner Support for additional Users and provide the Fusion username to which the User will be tied. 
- By tying the User to a Fusion username, the User passed into the API will then operate as the Fusion username.


---

# RESPONSES
## Success

**Response Code:**   HTTP 200 (OK)


**Example Response Body:**
```json
{
	"access_token": "eyJhb....t0Wvw",
	"expires_in": 3600,
	"token_type": "Bearer"
}
```

* Body is JSON containing the Bearer Token to be used for access.
* No refresh tokens are provided (currently)
* Tokens contain expiration (currently one hour), after which time a new token must be requested.


## Failure / Error
**Response Code:**  HTTP 401 (Unauthorized)	

Note: JSON in body of response can help to diagnose the cause of the failure.

**Example Response Body**

```json
{
	"error": "invalid_client"
}	
```
Reason
* The Client_ID is not recognized
* The Client_ID is recognized, but the Client_Secret is invalid

---

**Example Response Body**

```json
{
	"error": "invalid_grant",
	"error_description": "You do not have permission to use that Identity."
}
```
Reason
* The Client_ID is recognized, but the Partner or Customer is not authorized to access the specified User or Account.

---
---

**NOTES**


* Credentials for QA environment will not work in Production environment, and vice versa.
* Note that the bearer token value to be provided in the Authorization header does not include the quotes
* Contact Karmak Partner Support if you are unable to resolve the issue.

---
---

## Making the API Request

The base URL for all Unity API calls is as follows:

-   https://api.karmak.io/api/unity/{version}/unityapi/

-   See API documentation for specific URL requests

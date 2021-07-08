---
layout: post 
title: "Create and Update AP Vendors"  
category: "Accounting"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: Allow user to create and update AP Vendors in Fusion.
---

The AP Vendor API allows users to Create and Update AP Vendors records in Fusion

## Overview

The AP Vendor Endpoint API in Unity will allow users to create, update or get information about AP Vendor records in Fusion.   AP Vendor records in Fusion are Company wide and unique by the Vendor Number.

### POST
```
https://api.karmak.io/api/unity/{version}/unityapi/APVendor/Create
```

### PUT
```
https://api.karmak.io/api/unity/{version}/unityapi/APVendor/Update
```

### GET

Use the below link to access the Unity documentation to perform a GET on the AP Vendor Data Access Object to get information about Fusion AP Vendors

https://unity.karmak.io/AP-Vendor.html

### Specifications

#### POST

* The POST method will be used to create AP Vendor Records in Fusion.

* Only one AP Vendor record will be allowed in a single request call.

* A response will be provided with a message section that will outline a success or any issues that prevented the AP Vendor from being created.

* The Fusion Username used in the Unity API call will be used as the Add and Last Update User of the AP Vendor created.

* The Date and Time the Unity API call was made will be used as the Add Date and Last Update of the AP Vendor created.

* The AP Vendor record will be created in Fusion following the standard create logic of the APM90200 A/P Vendor form in Fusion outside of any specific rules listed in this section and the POST/PUT Request Fields Section below.

#### PUT

* The PUT method will be used to update A/P Vendor Records in Fusion.

* Only one A/P Vendor record will be allowed in a single request call.

* Only fields that are expected to be updated should be passed in outside of the required fields.

* In order to update an existing A/P Vendor record the user will be required to send in the AP Vendor Identity section of the request to find an existing AP Vendor.  If an existing AP Vendor is not found no update will be performed.

* A response will be provided with a message section that will outline a success or any issues that prevented the AP Vendor from being updated.

* The Fusion Username used in the Unity API call will be used as the Last Update User of the A/P Vendor created.

* The Date and Time the Unity API call was made will be used as the Last Update of the A/P Vendor created.

### Request Fields

| Field                | Field Type | Required | Length   | POST Business Rules and Defaults                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | PUT Business Rules and Defaults                                                                                                                                                                                         |
|----------------------|------------|----------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AP Vendor Identity   | Node       |    |    | This will be ignored in a POST when creating an AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                 | This section will be required when updating an AP Vendor as it will be used to look up the existing AP Vendor in Fusion.                                                                                                |
| Vendor               | string     | Yes      | 10       |     | This is the AP Vendor that is being looked up to perform an update to.                                                                                                                                                  |
|    |      |    |    |     | |
| Main Body            | Node       |    |    |     | |
| Vendor               | string     | Yes      | 10       | This is the AP Vendor Number being created.  Pass in the value of “New” to indicate you want to assign the new AP Vendor Number from the Next AP Vendor Number from the Enterprise setup.  If the Enterprise is not set to allow a company to assign an AP Vendor Number then this should be ignored and always create the AP Vendor with the next AP Vendor Number from the Enterprise setup.  If assigning of an AP Vendor is allowed via the Enterprise Record then a unique value must be provided.   | This value will be ignored on an update as the AP Vendor Number is not allowed to be updated in Fusion.                                                                                                                 |
| Company Name         | string     | Yes      | 100      | This is the Company Name of the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | This is the Company Name the looked up AP Vendor will be updated with.                                                                                                                                                  |
| Quick Lookup         | string     |    | 25       | This is a Quick Lookup value used for the AP Vendor.  If this value is left blank or not provided then use the 1st 25 characters of the Company Name                                                                                                                                                                                                                                                                                                                                                      | This is the Quick Lookup Value that looked up AP Vendor will be updated with.                                                                                                                                           |
| Payment Term         | string     | Yes      |  50      | This is the Payment Term of the AP Vendor.  This must match a valid Payment Term setup in Fusion which is user defined.                                                                                                                                                                                                                                                                                                                                                                                   | This is the Payment Term the looked up AP Vendor will be updated to.   This must match a valid Payment Term setup in Fusion which is user defined.                                                                      |
| Established Date     | Date       |    | MMDDYYYY | This the Established Date of the AP Vendor.                                                                                                                                                                                                                                                                                                                                                                                                                                                               | This is the Established Date the looked up AP Vendor will be updated with.                                                                                                                                              |
| Physical Address 1   | string     | Yes      |  100     | This is the Physical Address 1 of the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                           | This is the Physical Address 1 the the looked up AP Vendor will be updated with.                                                                                                                                        |
| Physical Address 2   | string     | No       |  100     | This is the Physical Address 2 of the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                           | This is the Physical Address 2 the the looked up AP Vendor will be updated with.                                                                                                                                        |
| Physical City        | string     | Yes      | 100      | This is the Physical City of the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                                | This is the Physical City the looked up AP Vendor will be updated with.                                                                                                                                                 |
| Physical Region      | string     | Yes      | 6        | This is the Physical Region of the AP VendorThis must match a valid Region setup in Fusion.  Fusion provides standard regions but allows user to setup additional regions as needed.                                                                                                                                                                                                                                                                                                                      | This is the Physical Region the looked up AP Vendor will be updated with.  This must match a valid Region setup in Fusion.  Fusion provides standard regions but allows user to setup additional regions as needed.     |
| Physical Postal Code | string     | Yes      | 15       | This is the Physical Postal Code of the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                         | This is the Physical Postal Code the looked up AP Vendor will be updated with.                                                                                                                                          |
| First Name           | string     | No       | 100      | This is the First Name of the Contact on the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                    | This is the First Name of the Contact on the AP Vendor that will be updated.                                                                                                                                            |
| Last Name            | string     | No       | 100      | This is the Last Name of the Contact on the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                     | This is the Last Name of the Contact on the AP Vendor that will be updated.                                                                                                                                             |
| Office Phone         | string     | No       | 30       | This is the Office Phone of the Contact on the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                  | This is the Office Phone of the Contact on the AP Vendor that will be updated.                                                                                                                                          |
| Shop Phone           | string     | No       | 30       | This is the Shop Phone of the Contact on the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                    | This is the Shop Phone of the Contact on the AP Vendor that will be updated.                                                                                                                                            |
| Cell Phone           | string     | No       | 30       | This is the Cell Phone of the Contact on the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                    | This is the Cell Phone of the Contact on the AP Vendor that will be updated.                                                                                                                                            |
| Fax                  | string     | No       | 30       | This is the Fax of the Contact on the AP Vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                           | This is the Fax of the Contact on the AP Vendor that will be updated.                                                                                                                                                   |
| EMail                | string     | No       | 100      | This is the Email Address of the Contact on the AP Vendor.  This must be in a valid Email format.                                                                                                                                                                                                                                                                                                                                                                                                         | This is the Email Address of the Contact on the AP Vendor that will be updated.  This must be in a valid Email format.                                                                                                  |
| Is1099Required       | boolean    | No       |        | (Requires Fusion v3.62.1 or later) This sets the flag is 1099 is required for the vendor                                                                                                                                                                                                                                                                                                                                                                                                                                                         | This is the Fax of the Contact on the AP Vendor that will be updated.                                                                                                                                                   |
| IncomeTypeID         | integer    | No       |       | (Requires Fusion v3.62.1 or later) This is the income type of the vendor, please see the list below                                                                                                                                                                                                                                                                                                                                                                                                         | This is the Email Address of the Contact on the AP Vendor that will be updated.  This must be in a valid Email format.                                                                                                  |

**IncomeTypeID is a universal table**
 (1, 'Cancellation of Debt (1099C)')
 (2, 'Federal income tax withheld')
 (3, 'Medical and health care payments')
 (4, 'Gross proceeds paid to an attorney')
 (5, 'Interest (1099INT)')
 (6, 'Nonemployee compensation')
 (7, 'Other income')
 (8, 'Rents')
 (9, 'Royalties')
 (10, 'Nonqualified deferred compensation')


### POST Request
```json
{              
               "Vendor":"Pool",
               "CompanyName":"Pool Rentals LLC",
               "QuickLookup":"SMP",
               "PaymentTerm":"Net 30",
               "EstablishedDate":"08/18/2020",
               "PhysicalAddress1":"100 Karmak Plaza",
               "PhysicalAddress2":"P.O Box 16",
               "PhysicalCity":"Carlinville",
               "PhysicalRegion":"IL",
               "PhysicalPostalCode":"62626",
               "FirstName":"Stephanie",
               "LastName":"Pool",
               "officePhone":"2178551212",
               "ShopPhone":"2178551212",
               "CellPhone":"2178551212",
               "Fax":"2178551212",
               "Email":"testsp@outlook.com"                  
			   "Is1099Required":true,
               "IncomeTypeID": "3"
                }
```

### POST Response
```json
{
    "Status": "A/P Vendor created successfully.",
    "Message": null
}
```

### PUT Request
```json
{
    "Identity":
         {
               "Vendor":"1004"
         },
               
               "PhysicalAddress1":"111 Karmak Plaza",
               "PhysicalAddress2":"P.O Box 17",
               "PhysicalCity":"Carlinville",
               "PhysicalRegion":"IL",
               "PhysicalPostalCode":"62626",
               "FirstName":"Steph",
               "LastName":"Pool",
               "officePhone":"8002527788",
               "ShopPhone":"8002527788",
               "CellPhone":"8002527788",
               "Fax":"8002527788",
               "Email":"test@outlook.com"
			   "Is1099Required":true,
               "IncomeTypeID": "8" 
                }
```

### PUT Response	
```json
{
    "Status": "A/P Vendor updated.",
    "Message": null
}
```
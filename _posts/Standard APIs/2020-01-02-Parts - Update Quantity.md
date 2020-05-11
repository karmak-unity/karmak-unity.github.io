---
layout: post
title: "Update Part Quantity"
category: "Parts" 
icon: "icon-gear"
type: "api" 
comments: false
description:  Update available quantity on an active Fusion part
---

---
The PUT method will be used to update available quantity on an active Fusion part. 


### PUT Method
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/udpatepartquantity
```


#### Restrictions
-   Multiple parts can be updated in a single PUT request

-   If part is sent in multiple times in a single request, an error will be returned stating that the same part is not allowed to be updated multiple times in a single request.

-   The parts transaction reason code will be 'PARTQTYAPI'.

---


| **JSON API Map**      | **Description**                                                                        | **Data Type ** | **Required?** | **Field Length/Format**          |
|-----------------------|----------------------------------------------------------------------------------------|----------------|---------------|----------------------------------|
|  "Branch"             | Branch where quantity is to be updatedand must be a valid Fusion branch.                                               | String         | Required      | Up to 10 alphanumeric characters |
|  "PartNumber"         | Part number which will be updated. Must be valid part number, and Status must be Active in Fusion                                                      | String         | Required      | Up to 50 alphanumeric characters |
|  "Supplier"           | Valid supplier of part number which will be updated                                          | String         | Required      | Up to 20 alphanumeric characters |
|  "QuantityAvailable"  | New quantity available value to be set in Fusion (cannot be equal to current quantity)<BR>Must not be less than zero <BR> -   Must be whole number<BR>-   No alpha or special characters<BR>-   Cannot be equal to current quantity | Integer        | Required      | Up to 10 numeric characters      |

### Sample PUT Request
```json	
[
    {
    "Branch" : "01",
    "PartNumber" : "SBC-23",
    "Supplier" : "ALLPARTS",
    "QuantityAvailable" : 5
    },
    {
    "Branch" : "BADBRANCH",
    "PartNumber" : "GOODPART",
    "Supplier" : "ALLPARTS",
    "QuantityAvailable" : 5
    },
    {
    "Branch" : "01",
    "PartNumber" : "BADPART",
    "Supplier" : "ALLPARTS",
    "QuantityAvailable" : 12
    },
    {
    "Branch" : "01",
    "PartNumber" : "INACTIVEPART",
    "Supplier" : "ALLPARTS",
    "QuantityAvailable" : 12
    },
    {
    "Branch" : "01",
    "PartNumber" : "GOODPART",
    "Supplier" : "BADSUPPLIER",
    "QuantityAvailable" : 9
    },
    {
    "Branch" : "01",
    "PartNumber" : "75-23",
    "Supplier" : "ALLPARTS",
    "QuantityAvailable" : -5
    },
    {
    "Branch" : "01",
    "PartNumber" : "12D-23",
    "Supplier" : "ALLPARTS",
    "QuantityAvailable" : 3.5
    },
    {
    "Branch" : "SAMEBRANCH",
    "PartNumber" : "SAMEPART",
    "Supplier" : "SAMESUPPLIER",
    "QuantityAvailable" : 3
    },
    {
    "Branch" : "SAMEBRANCH",
    "PartNumber" : "SAMEPART",
    "Supplier" : "SAMESUPPLIER",
    "QuantityAvailable" : 4
    }
]
```

### Response Code (200 OK)
```json
[
    {
    "Branch" : "01",
    "PartNumber" : "SBC-23",
    "Supplier" : "ALLPARTS",
    "Status" : "Success"
    },
    {
    "Branch" : "BADBRANCH",
    "PartNumber" : "GOODPART",
    "Supplier" : "ALLPARTS",
    "Status" : "ERR",
    "Message" : "branch BADBRANCH is invalid"
    },
    {
    "Branch" : "01",
    "PartNumber" : "BADPART",
    "Supplier" : "ALLPARTS",
    "Status" : "ERR",
    "Message" : "part number BADPART is invalid"
    },
    {
    "Branch" : "01",
    "PartNumber" : "INACTIVEPART",
    "Supplier" : "ALLPARTS",
    "Status" : "ERR",
    "Message" : "part number INACTIVEPART is inactive"
    },
    {
    "Branch" : "01",
    "PartNumber" : "GOODPART",
    "Supplier" : "BADSUPPLIER",
    "Status" : "ERR",
    "Message" : "supplier BADSUPPLIER is invalid"
    },
    {
    "Branch" : "01",
    "PartNumber" : "75-23",
    "Supplier" : "ALLPARTS",
    "Status" : "ERR",
    "Message" : "quantity cannot be negative"
    },
    {
    "Branch" : "01",
    "PartNumber" : "12D-23",
    "Supplier" : "ALLPARTS",
    "Status" : "ERR",
    "Message" : "quantity must be a whole number"
    },
    {
    "Branch" : "SAMEBRANCH",
    "PartNumber" : "SAMEPART",
    "Supplier" : "SAMESUPPLIER",
    "Status" : "ERR",
    "Message" : "multiple updates to the same part are not allowed in the same request"
    },
    {
    "Branch" : "SAMEBRANCH",
    "PartNumber" : "SAMEPART",
    "Supplier" : "SAMESUPPLIER",
    "Status" : "ERR",
    "Message" : "multiple updates to the same part are not allowed in the same request"
    }
]
```
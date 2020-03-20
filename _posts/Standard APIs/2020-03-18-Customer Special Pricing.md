---
layout: post
title: "Customer Special Pricing"
category: "Customer" 
icon: "icon-user"
type: "api" 
comments: false
description:   Allows users to create or update customer special pricing records in Fusion.
---

---

Customer Special Pricing API allows users to create or update customer special pricing records in Fusion.


**REQUIRED FUSION VERSION 3.59.30.0 or HIGHER**

Customer Special Pricing API supports the PUT and the POST method.

### Create
#### POST and PUT
- Note: The PUT method will overwrite an existing record

```
https://api.karmak.io/api/unity/{version}/unityapi/CustomerSpecialPricing/Create
```

### Update
#### POST
```
https://api.karmak.io/api/unity/{version}/unityapi/CustomerSpecialPricing/Update
````

### BUSINESS RULES
---

Customer Special Pricing records created via an API **must** define a Pricing Target and a Pricing Strategy.
-   Pricing Target - the target to which the record will apply, either a Customer Price Type, or Customer.
    -   Customer Price Type
    -   Customer
-   Pricing Strategy - the type of pricing for which the record is created
    -   Cost Matrix
    -   Velocity
    -   Price Data
-   Only one Pricing Target can be passed in the request.
-   Only one Pricing Strategy can be passed in the request.
-   Both a Pricing Target and a Pricing Strategy must be passed.

When Pricing Target and Pricing Strategy have been defined, a specific dataset must be passed in the payload to create the customer special pricing record.

### Customer Price Type

To create or update a customer special pricing record by Customer Price Type:
-   Pass in the Customer Price Type to which the record applies
    -   A list of valid Customer Price Types can be obtained using the Quick List data access API

#### Customer
To create or update a customer special pricing record by Customer:
-   Pass in the Customer Key and Customer base branch code to which the record applies
    -   A valid list of customers can be obtained using the Customer data access API

#### Cost Matrix
To create or update a customer special pricing record for Cost Matrix Code:
-   Pass in the Cost Matrix Code to which the record applies
    -   A list of valid Cost Matrix Codes can be obtained using the Quick List data access API
-   When Pricing Strategy = Cost Matrix Code, the following fields can be passed, but are not required:
    -   Expiration Date
    -   Internal Note

#### Velocity
To create or update a customer special pricing record by Velocity Type Code:
-   Pass in the Velocity Code Type to which the record applies
    -   A valid list of Velocity Type Codes can be obtained using the VelocityCodeTypes data access API
	
-   When Pricing Strategy = Velocity Type Code, the following fields can be passed, but are not required:
    -   Expiration date
    -   Internal Note

### **Price Data**
To create or update a customer special pricing record by Price Data:
-   There are multiple pricing paths in the Price Data strategy, and the payload part criteria are specific to each.


To create or update **Price Level** pricing
-   A price level MUST be passed


| **Data Element** | **Appearance** | **Business Rules** |
|----------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| Price Level                | Required | Must be one of the following: Replacement Cost, Price 7, Price 6, Price 5, Price 4, Price 3, Price 2, Price 1, List |
| Service Uses Parts Pricing | Optional |                                                                                                                     |
| Service Level              | Optional | Passed only when Service Uses Parts Pricing = False                                                                 |
| Additional Multiplier      | Optional | If passed, must be greater than 0.                                                                                  |
| Supplier(s)                | Optional | If Supplier is passed, Price Group must not be present.                                                             |
| Price Group(s)             | Optional | If Price Group is passed, Supplier must not be present.                                                             |
| Part Type                  | Optional | Must be one of the following: Part, Exchange, Core                                                                  |
| Stock Class                | Optional | Must not exceed 10 characters.                                                                                      |
| Code 1                     | Optional | Must not exceed 10 characters.                                                                                      |
| Code 2                     | Optional | Must not exceed 10 characters.                                                                                      |
| Expiration Date            | Optional |                                                                                                                     |
| Internal Note              | Optional | Must not exceed 100 characters.                                                                                     |

---

---

To create or update **Supplier** pricing
-   A Supplier or Suppliers must be passed
-   A Price Level must be passed

| **Data Element** | **Appearance** | **Business Rules** |
|----------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| Price Level                | Required                             | Must be one of the following: Replacement Cost, Price 7, Price 6, Price 5, Price 4, Price 3, Price 2, Price 1, List |
| Service Uses Parts Pricing | Optional                             |                                                                                                                     |
| Service Level              | Optional                             | Passed only when Service Uses Parts Pricing = False                                                                 |
| Additional Multiplier      | Optional                             | If passed, must be greater than 0.                                                                                  |
| Supplier(s)                | Required to set pricing for Supplier | If Supplier is passed, Price Group must not be present.                                                             |
| Part Type                  | Optional                             | Must be one of the following: Part, Exchange, Core                                                                  |
| Stock Class                | Optional                             | Must not exceed 10 characters.                                                                                      |
| Code 1                     | Optional                             | Must not exceed 10 characters.                                                                                      |
| Code 2                     | Optional                             | Must not exceed 10 characters.                                                                                      |
| Expiration Date            | Optional                             |                                                                                                                     |
| Internal Note              | Optional                             | Must not exceed 100 characters.                                                                                     |

---

---

To create or update **Price Group** pricing
-   A Price Group or Price Groups must be passed
-   A Price Level must be passed


| Price Level                | Required                               | Must be one of the following: Replacement Cost, Price 7, Price 6, Price 5, Price 4, Price 3, Price 2, Price 1, List |
|----------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Service Uses Parts Pricing | Optional                               |                                                                                                                     |
| Service Level              | Optional                               | Passed only when Service Uses Parts Pricing = False                                                                 |
| Additional Multiplier      | Optional                               | If passed, must be greater than 0.                                                                                  |
| Price Group(s)             | Required to set pricing by Price Group | If Price Group is passed, Supplier must not be present.                                                             |
| Part Type                  | Optional                               | Must be one of the following: Part, Exchange, Core                                                                  |
| Stock Class                | Optional                               | Must not exceed 10 characters.                                                                                      |
| Code 1                     | Optional                               | Must not exceed 10 characters.                                                                                      |
| Code 2                     | Optional                               | Must not exceed 10 characters.                                                                                      |
| Expiration Date            | Optional                               |                                                                                                                     |
| Internal Note              | Optional                               | Must not exceed 100 characters.                                                                                     |

---

---

To create or update **Part Number** pricing
-   A Part Number must be passed
-   A Price Level must be passed *or* a Contract Price must be passed


| **Data Element** | **Appearance** | **Business Rules** |
|----------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| Price Level                | Conditional | If Contract Price is passed, Price Level must not be present. If no Contract Price is passed, Price Level is required. |
| Service Uses Parts Pricing | Optional    |                                                                                                                        |
| Service Level              | Optional    | Passed only when Service Uses Parts Pricing = False                                                                    |
| Additional Multiplier      | Optional    | If passed, must be greater than 0.                                                                                     |
| Part Number                | Required    | Must be valid Fusion part.                                                                                             |
| Contract Price             | Optional    | If Price Level is passed, Contract Price must not be present.                                                          |
| Always Use Contract Price  | Optional    | May only be present if Contract Price is passed.                                                                       |
| Expiration Date            | Optional    |                                                                                                                        |
| Internal Note              | Optional    | Must not exceed 100 characters.                                                                                        |

 

### Request Samples
--------------------
-   Pricing Target - Customer Price Type
-   Pricing Strategy - Price Data, for Cost Matrix pricing

```json
[
    {
        "ExpirationDate": "2020-3-24",
        "PricingTarget": {
        	"customerPriceType" : "Cash"
        },
        "PricingStrategy" : {
        	"CostMatrixCode" : "A"
        },
        "InternalNote": "test note"
    }
]
```

---

---

-   Pricing Target - Customer Price Type
-   Pricing Strategy - Price Data, for Velocity pricing


```json
[
    {
        "ExpirationDate": "2020-1-24",
        "PricingTarget": {
        	"customerPriceType" : "General Accounts"
        },
        "PricingStrategy" : {
        	"VelocityCode" : "Zebra"
        },
        "InternalNote": "test note"
    }
]
```

---

---

-   Pricing Target - Customer Price Type
-   Pricing Strategy - Price Data
    -   Price Level set to Price 5
    -   Multiple Suppliers are passed
    -   Part Type = Part


```json
[
    {
        "ExpirationDate": "2020-3-24",
        "PricingTarget": {
            "customerPriceType" : "Pinnacle Accounts"
        },
        "PricingStrategy" : {
            "priceData" : {
                "ServiceUsesPartsPricing" : "false",
                "priceInfo" : {
                    "PartsLevel" : "Price 5"
                }
            },
            "partCriteria" : {
                "suppliers" : [
                        {
                            "SupplierCode" : "00OP1"
                        },
                        {
                            "SupplierCode" : "00OP2"
                        }
                    ],
                "PartType" : "Part"
            }
        },
        "InternalNote": "test note"
}

]
```

---

---

-   Pricing Target - Customer
-   Pricing Strategy - Price Data
    -   Parts Level set to List

```json
[
    {
        "ExpirationDate": "2020-1-24",
        "PricingTarget": {
            "CustomerKey": "1061",
            "CustomerBaseBranchCode": "01"
        },
        "PricingStrategy" : {
            "priceData" : {
                "ServiceUsesPartsPricing" : "false",
                "priceInfo" : {
                    "PartsLevel" : "List"
                }
            },
            "partCriteria" : {
                "suppliers" : [
                        {
                            "SupplierCode" : "00OP1"
                        }
                        
                    ]
                
            }
        },
        "InternalNote": "test note"
}

]
```

---

---

-   Pricing Target - Customer Price Type
-   Pricing Strategy - Price Data
    -   Expiration Date Passed
    -   Multiple Suppliers are passed
    -   Part Type = Part
    -   Service Price Level set to Price 5

```json
[
    {
        "ExpirationDate": "2020-3-24",
        "PricingTarget": {
            "customerPriceType" : "Pinnacle Accounts"
        },
        "PricingStrategy" : {
            "priceData" : {
                "ServiceUsesPartsPricing" : "false",
                "priceInfo" : {
                    "ServiceLevel" : "Price 5"
                }
            },
            "partCriteria" : {
                "suppliers" : [
                        {
                            "SupplierCode" : "00OP1"
                        },
                        {
                            "SupplierCode" : "00OP2"
                        }
                    ],
                "PartType" : "Part"
            }
        },
        "InternalNote": "test note"
}
]
```

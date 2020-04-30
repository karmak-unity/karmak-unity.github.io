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

## Create
### POST and PUT
- Note: The PUT method will overwrite an existing record

```
https://api.karmak.io/api/unity/{version}/unityapi/CustomerSpecialPricing/Create
```

## Update
### PUT
```
https://api.karmak.io/api/unity/{version}/unityapi/CustomerSpecialPricing/Update
````

## BUSINESS RULES
---

Customer Special Pricing records created via an API **must** define a Pricing Target and a Pricing Strategy.

-   Only one Pricing Target can be passed in the request.
-   Only one Pricing Strategy can be passed in the request.
-   Both a Pricing Target and a Pricing Strategy must be passed.

 

---

### Pricing Target 
The target to which the record will apply, either a Customer Price Type, or Customer.


#### Customer Price Type

To create or update a customer special pricing record by Customer Price Type:
-   Pass in the Customer Price Type to which the record applies
    -   A list of valid Customer Price Types can be obtained using the Quick List data access API

#### Customer
To create or update a customer special pricing record by Customer:
-   Pass in the Customer Key and Customer base branch code to which the record applies
    -   A valid list of customers can be obtained using the Customer data access API



---


### Pricing Strategy
The type of pricing for which the record is created (Cost Matrix, Velocity, Part Criteria)



#### Cost Matrix
To create or update a customer special pricing record for Cost Matrix Code:
-   Pass in the Cost Matrix Code to which the record applies.
    -   A list of valid Cost Matrix Codes can be obtained using the Quick List data access API.


#### Velocity
To create or update a customer special pricing record by Velocity Type Code:
-   Pass in the Velocity Code Type to which the record applies.
    -   A valid list of Velocity Type Codes can be obtained using the VelocityCodeTypes data access API.
	

#### Part Criteria
To create or update a customer special pricing record by Price Data:
-   There are multiple pricing paths in the part criteria strategy.
	- Note: in order to create or update Part Number pricing, you must also pass a price level or a Contract Price

---
---

| **Data Element** | **Business Rules** |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| PartsLevel                | Must be one of the following: Replacement Cost, Price 7, Price 6, Price 5, Price 4, Price 3, Price 2, Price 1, List |
| ServiceUsesPartsPricing 	|                                                                                                                     |
| ServiceLevel              | Passed only when Service Uses Parts Pricing = False                                                                 |
| Multiplier      			| If passed, must be greater than 0.                                                                                  |
| SupplierCode                | If Supplier is passed, Price Group must not be present.                                                             |
| PriceGroup          		| If Price Group is passed, Supplier must not be present.                                                             |
| PartType                  | Must be one of the following: Part, Exchange, Core                                                                  |
| StockClass                | Must not exceed 10 characters.                                                                                      |
| Code1                     | Must not exceed 10 characters.                                                                                      |
| Code2                     | Must not exceed 10 characters.                                                                                      |
| ExpirationDate            |                                                                                                                     |
| PartNumber                | Must be valid Fusion part.                                                                                          |
| Price             		| If Price Level is passed, Contract Price must not be present.                                                       |
| InternalNote              | Must not exceed 100 characters.                                                                                     |
| PricingTarget				|	|
| CustomerKey				|	|
| CustomerBaseBranchCode	|	|
| CustomerPriceType			|	|
| CostMatrixCode			|	|
| VelocityCode				|	|

---
---



## Request Samples
--------------------

If you call the POST method, an existing record is NOT overridden, if you call PUT method then override occurs

The general structure of the payload is as follows:
```json
[
    {
        "ExpirationDate": "04/30/2020",
        "PricingTarget": {  },
        "PricingStrategy": {  },
        "InternalNote": "This is my note."
    }
]
```

First determine what type of Pricing Target you are going to use, either Customer or Customer Price Type.


**PricingTarget for a Customer:**

```json
{
    "CustomerKey": "12345",
    "CustomerBaseBranchCode": "15"
}
```


**PricingTarget for a CustomerPriceType:**

```json
{
    "CustomerPriceType": "234abc"
}
```

Then you need to determine which Strategy you are going to use, Cost Matrix Code, Velocity Code, or Part Criteria.


**PricingStrategy for Cost Matrix Code:**

```json
{
    "CostMatrixCode": "25abc"
}
```


**PricingStrategy for Velocity Code:**

```json
{
    "VelocityCode": "01adb"
}
```

For Part Criteria you have a few more choices to make, the Price Info and the Part Criteria to which it should apply.
  
You will need to determine which PriceInfo you are going to specify for this record, Contract Price, Parts Price Level, or Service Price Level.

Also, the PartCriteria does NOT have to be fully populated, this is as restrictive as needed to establish the scenario(s) this pricing record should cover.


**PricingStrategy for Part Criteria:**

```json
{
    "PriceData": {
        "ServiceUsesPartsPricing": "false",
        "PriceInfo": {}
    },
    "PartCriteria": {
        "Suppliers": [  //Only Supplier OR PriceGroup can be used not both
            {
                "SupplierCode": "bc23"
            }
        ],
        "PriceGroups": [ //Only Supplier OR PriceGroup can be used not both
            {
                "PriceGroup": "87asdf"
            }
        ],
        "PartType": "part",
        "StockClass": "123abc",
        "Code1": "456def",
        "Code2": "ghj789",
        "PartNumber": "3nva34"  //If PartNumber is used then at least one Supplier is required
    }
}
```


**PriceInfo for Contract Price:**

```json
{
    "Price": "1.00"
}
```


**PriceInfo for Parts Price Level**

```json
{
    "PartsLevel": "Price 1",
    "Multiplier": "1.5"
}
```


**PriceInfo for Service Level**

```json
{
    "ServiceLevel": "Price 1",
    "Multiplier": "1.5"
}
```


**Pricing Target is Customer, Pricing Strategy is Velocity Code example:**

```json
[
    {
        "ExpirationDate": "04/30/2020",
        "PricingTarget": {
            "CustomerKey": "12345",
            "CustomerBaseBranchCode": "15"
        },
        "PricingStrategy": {
            "VelocityCode": "01adb"
        },
        "InternalNote": "This is my note."
    }
]
```


**Pricing Target is Customer Price Type, Pricing Strategy is Velocity Code example:**

```json
[
    {
        "ExpirationDate": "04/30/2020",
        "PricingTarget": {
            "CustomerPriceType": "234abc"
        },
        "PricingStrategy": {
            "VelocityCode": "01adb"
        },
        "InternalNote": "This is my note."
    }
]
```
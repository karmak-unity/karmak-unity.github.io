---
layout: post
title: "Quick Lists (Helper)"
category: "Helper APIs" 
icon: "icon-question1"
type: "data_access"
comments: false
description:   Allow the user to pull back Quick List options from Fusion
---

---

---

**Note: Minimum Fusion v3.59.30.0 or higher**

The Quick List API is a GET method API that will allow the user to pull back Quick List options from Fusion, to be used in support of other Unity API calls into Fusion. The Quick List table includes information often stored in dropdown lists in various Fusion applications, where the user has defined the options present in the list.

---

---

The below data can be gathered using the Quick List API, and used when necessary to support making Unity API calls.

| Quick List Type | Quick List ID | Quick List Code |
|-----------------------------|----|----------|
| A/P Vendor Group            | 12 | APM90250 |
| A/R Invoice Import Item     | 31 | ARM90360 |
| Backorder Priority          | 17 | INV91700 |
| Cost Matrix Codes           | 25 | PRC93600 |
| Cross Reference Message     | 19 | INV91650 |
| Customer Price Type         | 20 | PRC90200 |
| Fixed Asset Category        | 24 | FAD90100 |
| Fuel Type                   | 27 | FBM11000 |
| Industry Type               | 11 | ARM90350 |
| L/R Equipment Class         | 2  | UNT94010 |
| L/R Equipment Type          | 1  | UNT94000 |
| L/R Finance Source          | 30 | LRM20500 |
| L/R Fleet Type              | 9  | UNT94020 |
| L/R Unit Status             | 8  | UNT94020 |
| Labor Accounting            | 13 | GLM90700 |
| Notes Payable Group         | 26 | NPM99250 |
| Order Group                 | 16 | INV90065 |
| Parts Accounting            | 14 | GLM90800 |
| Parts Lost Sales Reasons    | 21 | INV91855 |
| Price Group                 | 6  | INV90055 |
| Price Rounding Code         | 28 | INV91070 |
| Quantity Adjustment Reason  | 15 | INV90060 |
| Return Reason               | 5  | INV91800 |
| Territory                   | 29 | ARM90355 |
| Unit of Measure             | 5  | INV90050 |

<BR>
<BR>

### The dataset returned in the Quick List API is as follows:

| Field | Definition
|------------------------|----------------------------------------------------------------------------------------|
| QuickListItemID        | Database ID for QuickList item                                                         |
| QuickListID            | Database ID for QuickList                                                              |
| Name                   | QuickList name                                                                         |
| QuickListCode          | QuickList Code (Application Number)                                                    |
| Value                  | QuickList item name                                                                    |
| SortOrder              | Sort order of QuickList item                                                           |
| Inactive               | Is QuickList item inactive                                                             |
| AddUserID              | Add User of the record by User ID                                                      |
| AddUser                | Add User of the record                                                                 |
| AddDate                | Add date of the record                                                                 |
| UpdateUserID           | Last update user ID of the record                                                      |
| UpdateUser             | Last update user name of the record                                                    |
| LastUpdate             | Last update date of the record                                                         |
| IsSystem               |                                                                                        |
| AliasedQuickListItemID |                                                                                        |
| IsImpactTotalLostSales | Does QuickList item impact total lost sales? (Parts Lost Sales Reasons QuickList only) |
| LeaseRentalFleetType   | Fleet Type (L/R Fleet Type QuickList only)                                             |

 
---
---

### Base Request

#### Url

```
/frw/QuickListItemFull
```

### Base Response
```json
{
    "QuickListItemID": int,
    "QuickListID": int,
    "Name": "List Name",
    "QuickListCode": "CODE000",
    "Value": "List Value",
    "SortOrder": int,
    "Inactive": true/false,
    "Data": int,
    "AddDate": "2000-12-30T00:00:00.000",
    "AddUserID": int,
    "AddUser": "username",
    "UpdateUserID": int,
    "UpdateUser": "username",
    "LastUpdate": "2000-12-30T00:00:00.000",
    "AddDateTimeZone": -0.00,
    "LastUpdateTimeZone": -0.00,
    "IsSystem": true/false,
    "AliasedQuickListItemID": int/null
}
```

## Examples

### L/R Unit Status Request
```c#
/frw/QuickListItemFull?select=QuickListItemID,Value&filter=QuickListID[EQ]8
```

### L/R Unit Status Response

#### Body (Example data used, actual data may vary!)
```json
[
    {
        "QuickListItemID": 164,
        "Value": "New"
    },
    {
        "QuickListItemID": 165,
        "Value": "Old"
    },
    {
        "QuickListItemID": 189,
        "Value": "Down for Repairs"
    },
    {
        "QuickListItemID": 384,
        "Value": "Out of Service"
    }
]
```


### L/R Equipment Type Request
```c#
/frw/QuickListItemFull?select=QuickListItemID,Value&filter=QuickListID[EQ]1
```

### L/R Equipment Type Response

#### Body (Example data used, actual data may vary!)
```json
[
    {
        "QuickListItemID": 140,
        "Value": "Rental"
    },
    {
        "QuickListItemID": 148,
        "Value": "Lease"
    },
    {
        "QuickListItemID": 149,
        "Value": "Flatbed"
    },
    {
        "QuickListItemID": 150,
        "Value": "Van"
    },
    {
        "QuickListItemID": 151,
        "Value": "Sleeper"
    },
    {
        "QuickListItemID": 152,
        "Value": "Dump Truck"
    },
    {
        "QuickListItemID": 153,
        "Value": "Reefer"
    },
    {
        "QuickListItemID": 154,
        "Value": "Trailer"
    },
    {
        "QuickListItemID": 155,
        "Value": "Bus"
    },
    {
        "QuickListItemID": 156,
        "Value": "Inactive"
    },
    {
        "QuickListItemID": 214,
        "Value": "28' Reefer"
    },
    {
        "QuickListItemID": 215,
        "Value": "35' Reefer"
    },
    {
        "QuickListItemID": 216,
        "Value": "42' Reefer"
    },
    {
        "QuickListItemID": 217,
        "Value": "48' Reefer"
    },
    {
        "QuickListItemID": 218,
        "Value": "50' Reefer"
    },
    {
        "QuickListItemID": 219,
        "Value": "53' Reefer"
    },
    {
        "QuickListItemID": 220,
        "Value": "26' Dry Van"
    },
    {
        "QuickListItemID": 221,
        "Value": "28' Dry Van"
    },
    {
        "QuickListItemID": 222,
        "Value": "45' Dry Van"
    },
    {
        "QuickListItemID": 223,
        "Value": "48' Dry Van"
    },
    {
        "QuickListItemID": 224,
        "Value": "53' Dry Van"
    },
    {
        "QuickListItemID": 225,
        "Value": "48' Flatbed"
    },
    {
        "QuickListItemID": 226,
        "Value": "50' Flatbed"
    },
    {
        "QuickListItemID": 227,
        "Value": "53' Flatbed"
    },
    {
        "QuickListItemID": 228,
        "Value": "45' Reefer"
    },
    {
        "QuickListItemID": 293,
        "Value": "TA Day Cab Tractor"
    },
    {
        "QuickListItemID": 346,
        "Value": "53' DRY VANS AIRRIDE/SPRINGRIDE LONGDESC"
    }
]
```
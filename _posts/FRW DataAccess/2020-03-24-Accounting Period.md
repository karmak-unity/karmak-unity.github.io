---
layout: post
title: "Accounting Period"
category: "Accounts Payable" 
icon: "icon-shopping-bag"
type: "data_access"
comments: false
description:   Allow the user to query the status of an accounting posting period.
---

---

---

A GET API to query the status of an accounting posting period.

To query closed Posting Periods, set IsOpen = NO and IsFuture = NO.

| Field | Definition | Type |
|---|---|---|
| “AccountingPeriodID” | Accounting Period Unique ID                 | int         |
| “PeriodString”       | Posting Period                              | varchar(33) |
| “CorporationID”      | *informational only*                        | int         |
| “IsOpen”             | Determines if Posting Period is Open        | int         |
| “IsFuture”           | Determines if Posting Period is Future      | int         |
| “BeginDate”          | First day of Posting Period                 | datetime    |
| “EndDate”            | Last Day of Posting Period                  | datetime    |
| “IsFiscalPeriodOpen” | Determines if Fiscal Year is open or closed | bit         |

#### Sample Response
```json
{
	"AccountingPeriodID": 75,
	"PeriodString": "01/2009",
	"CorporationID": 1,
	"IsOpen": 0,
	"IsFuture": 0,
	"BeginDate": "2009-01-01T00:00:00",
	"EndDate": "2009-01-31T00:00:00",
	"IsFiscalPeriodOpen": false
}
```
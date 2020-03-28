---
layout: post
title: "Department (Helper)"
category: "Helper APIs" 
icon: "icon-question1"
type: "data_access"
comments: false
description:   Allow the user to query department details
---

---

---

A GET API to query department details.

| Field | Definition | Type |
|-------------------------------|-------------------------|--------------|
| “Department”       | Department identifier.                                                                                                                                                                           | varchar(10)  |
| “Name”             | Department name.                                                                                                                                                                                 | varchar(100) |
| “Department Type”  | Type of department; Account, Body Shop, L/R, Parts, Sales, or Service.                                                                                                                           | varchar(50)  |
| “Inactive”         | When set to TRUE, this field indicates that the department record is inactive (ie, no longer used or valid for entry); inactive departments will not appear in a selection list in applications. | bit          |
| “Add User”         | Username associated with the user who added the department record.                                                                                                                               | varchar(20)  |
| “Add Date”         | Date/time the department record was added.                                                                                                                                                       | datetime     |
| “Last Update User” | Username associated with the user who last updated the department record.                                                                                                                        | varchar(20)  |
| “Last Update Date” | Date/time the department record was last updated.                                                                                                                                                | datetime     |

 
#### Sample Department API Response

```json
{
	"Department": "45",
	"Name": "parts",
	"Department Type": "Parts",
	"Inactive": false,
	"Add User": "Morgan",
	"Add Date": "2017-05-25T15:36:23.637",
	"Last Update User": "Morgan",
	"Last Update Date": "2017-05-25T15:36:23.637"
}
```
---
layout: post
title: "View Users"
category : "Users"
icon: "icon-man"
type: "data_access" 
comments: false
description: Access to view all users by Branch
---

---
---

This data object is used to show all user information.

This information can be found in the Users program within the Fusion business system.

 
#### URL
```
/frw/Users
```
 <hr>
Field Details...

| **SQL Field Name**  | Field Type | **Column Description**                                                                                                 |
|---|---|
| User Name	 | varchar(20)| System User Name in Fusion |
| Language	 | varchar(50)| Default User Language |
| Technician	 | varchar(20)| |
| Inactive	 | bit| True / False is user active|
| Disabled	 | bit| True / False is user disabled|
| Employee	 | varchar(20)| |
| User Default Printer	 | varchar(220)| |
| Salutation	 | varchar(50)| User Salutation (mr, Mrs, ms, Sir) |
| First Name	 | varchar(100)| User First Name |
| Last Name	 | varchar(100)| User last name |
| Title	 | varchar(50)| |
| Middle Initial	 | varchar(1)| Users Middle Initial |
| Work Phone	 | varchar(30)| Work Phone |
| Fax	 | varchar(30)| Fax Number |
| Home Phone	 | varchar(30)| Home Phone NUmber |
| Pager	 | varchar(30)| User Pager / Beeper Number |
| E-mail Address	 | varchar(100)| User Email Address |
| Web Address	 | varchar(100)| Users website URL |
| Bill-to Address 1	 | varchar(100)|  This field displays the Primary Bill-To address line 1 of the customer record.  |
| Bill-to Address 2	 | varchar(100)| This field displays the Primary Bill-To Address line 2 of the customer record. |
| Bill-to City	 | varchar(100)| This field displays the Primary Bill-To City of the customer record.     |
| Bill-to Region	 | varchar(6)| This field displays the Primary Bill-To Region of the customer record. |
| Bill-to Postal Code	 | varchar(15)| This field displays the Primary Bill-To Postal Code of the customer record.  |
| Bill-to Country	 | varchar(35)| Billing Country location |
| Bill-to County	 | varchar(35)| Billing County for US  |
| Branch	 | varchar(10)| This field displays the code associated with a user base branch.  |
| Department	 | varchar(10)|This field displays the department associated with a user |
| User Group	 | varchar(50)| |
| Salesperson Legacy Link	 | varchar(20)| |
| Unit Salesperson	 | bit| True / false flag for permissions |
| Inside Service Salesperson	 | bit|True / false flag for permissions |
| Inside Parts Salesperson	 | bit| True / false flag for permissions|
| Lease Salesperson	 | bit| True / false flag for permissions|
| Rental Salesperson	 | bit| True / false flag for permissions|
| Department Administrative User	 | bit|True / false flag for permissions |
| Branch Administrative User	 | bit| True / false flag for permissions|
| Division Administrative User	 | bit|True / false flag for permissions |
| Corporate Administrative User	 | bit|True / false flag for permissions |
| Set Default	 | bit| |
| Add User	 | varchar(20)| |
| Add Date	 | datetime| Date User was created |
| Last Update User	 | varchar(20)| |
| Last Update Date	 | datetime| Date User was updated |
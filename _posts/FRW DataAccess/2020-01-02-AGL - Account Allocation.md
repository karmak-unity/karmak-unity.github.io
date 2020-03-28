---
layout: post
title: "Account Allocation"
category: "Accounting General Ledger" 
icon: "icon-money"
type: "data_access" 
comments: false
description: Display the allocation tables specified in Fusion, along with the allocation breakdown for each by Branch/Department and the list of breakdown accounts specified in the setup form of the Allocation Table
---

---

This data object is used to display the allocation tables specified in Fusion, along with the allocation breakdown for each by Branch/Department and the list of breakdown accounts specified in the setup form of the Allocation Table.  It also displays, for each allocation table, any GL account that it has been associated with in the setup form of the given GL account, along with the branch and/or department associated with that link.

This information comes from the Account Allocation and the Chart of Accounts programs within the Fusion business system.


#### URL
```
/frw/AccountAllocation
```
 
<hr>
Field Details...

| **SQL Field Name**   | **Column Description**                                                                                                                    |
|---|---|
| AccountDescription   | This field displays the account description of a GL account that the given allocation table has been associated with in Chart of Accounts.                                                                                                                                                                                          |
| AddDate              | This field displays the date on which the allocation table was added to the system.                                                                                                                                                                                                                                                 |
| AddUser              | This field displays the user name of the individual who added the allocation table.                                                                                                                                                                                                                                                 |
| BasedOn              | This field displays whether a variable allocation table is based on Year to Date, Transaction Period, or Prior Transaction Period, or for a fixed allocation table, displays Fixed Allocation.                                                                                                                                      |
| AllocationBranch     | This field displays the branch that a percentage amount will be allocated to.                                                                                                                                                                                                                                                       |
| AllocationDepartment | This field displays the department that a percentage amount will be allocated to.                                                                                                                                                                                                                                                   |
| AllocationName       | This field displays the name of the given allocation table.                                                                                                                                                                                                                                                                         |
| AllocationType       | This field displays whether the allocation table describes a fixed or variable allocation type.                                                                                                                                                                                                                                     |
| BreakdownAccounts    | This field displays the list of accounts specified in the allocation table for the allocation amount to be split between.                                                                                                                                                                                                           |
| GLAccount            | This field displays the account number of a GL account that the given allocation table has been associated with in Chart of Accounts.                                                                                                                                                                                               |
| GLBranch             | This field displays the branch that has been specified in Chart of Accounts when associating an allocation table with a GL Account. (When accounting is posted to the account in GL Account and this branch, a percentage will be allocated to the branch and/or department in Allocation Branch and Allocation Department.         |
| GLDepartment         | This field displays the department that has been specified in Chart of Accounts when associating an allocation table with a GL Account. (When accounting is posted to the account in GL Account and this department, a percentage will be allocated to the branch and/or department in Allocation Branch and Allocation Department. |
| IsDistributeEvenly   | This field displays whether the given allocation table distributes evenly between the branches and/or departments listed in the allocation table.                                                                                                                                                                                   |
| LastUpdateDate       | This field displays the date on which the allocation table was last updated.                                                                                                                                                                                                                                                        |
| UpdateUser           | This field displays the user name of the individual who last updated the allocation table.                                                                                                                                                                                                                                          |
| PercentAllocated     | This field displays the percentage that has been allocated to the location specified in the Branch and/or Department fields, for allocation tables with an allocation type of fixed.                                                                                                                                                |
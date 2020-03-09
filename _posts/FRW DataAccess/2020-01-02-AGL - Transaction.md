---
layout: post
title: "General Ledger Transaction"
category: "Accounting General Ledger" 
icon: "icon-money"
type: "data_access" comments: falsedescription: Display the allocation tables specified in Fusion, along with the allocation breakdown for each by Branch/Department and the list of breakdown accounts specified in the setup form of the Allocation Table
---
## Accounting General Ledger Transaction
---

This data object is used to show all GL detail transactions in the Fusion
business system.

This information is found within the Accounting General Ledger Transaction
program within the Fusion business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**         | **Column Description**                                                                                                                                 |
|---|---|
| AccountType                | This field displays the general ledger account type: assets, liability, capital, other revenue, sales revenue, other expenses, and cost of goods sold. |
| AddUser                    | This field displays the user name that added the record.                                                                                               |
| Amount                     | This Field Displays the amount of the general ledger transaction.                                                                                      |
| Branch                     | This field displays the branch associated with a general ledger transaction.                                                                           |
| BranchDescription          | This field displays the branch description of a given general ledger transaction.                                                                      |
| CheckNumber                | This field displays the check number used in a given transaction.                                                                                      |
| CompanyName                | This field displays the company name of an A/P vendor associated with the general ledger transaction.                                                  |
| Control                    | This field displays the control value for a given general ledger transaction.                                                                          |
| CustomerName               | This field displays the A/R customer's name from the customer record.                                                                                  |
| CustomerNumber             | This field displays the identifying number attached to a customer.                                                                                     |
| DaysOld                    | This field displays the difference between the invoice due date and the current date.                                                                  |
| Department                 | This field displays the department associated with a general ledger transaction.                                                                       |
| DepartmentType             | This field displays the pre-defined list that a user must tie deferrment to.                                                                           |
| FiscalYear                 | This field displays the fiscal year being observed.                                                                                                    |
| GLAccount                  | This field displays the general ledger account number associated with the general ledger transaction.                                                  |
| GLDescription              | This field displays the general ledger account description associatd with the general ledger transaction.                                              |
| Journal                    | This field displays the journal source code for a general ledger transaction.                                                                          |
| JournalReference           | This field displays the reference number attached to a given journal.                                                                                  |
| UpdateUser                 | This field displays the user name of the individual who made the update.                                                                               |
| NumericCode                | This field displays the department code associated with the general ledger account number.                                                             |
| OrderBranch                | This field displays the branch in which the transactions originated from.                                                                              |
| OverridePostingDescription | This field displays the override description for a given transaction.                                                                                  |
| PostDate                   | This field displays the date on which appreciation was posted for a fixed asset.                                                                       |
| PostMonth                  | This field displays the month in which a transaction was posted, in MM format.                                                                         |
| PostYear                   | This field displays the year in which a transaction was posted, in YYYY format.                                                                        |
| PostingDescription         | This field displays a posting description for an Accounts Payable invoice.                                                                             |
| PostingPeriod              | This field displays the posting period that was used to depreciate a fixed asset.                                                                      |
| PostingSequence            | This field displays the sequence number attached to a posting.                                                                                         |
| IsReconciled               | This field displays whether or not an entry has been reconciled.                                                                                       |
| SourceApplication          | This field displays the application used to create the general ledger posting.                                                                         |
| TransactionDate            | This field displays the date on which a transaction was created.                                                                                       |
| TransactionDescription     | This field displays the description of a transaction.                                                                                                  |
| User                       | This field displays the user name of the user who posted a transaction.                                                                                |
| Vendor                     | This field displays the vendor attached to a given A/P invoice.                                                                                        |
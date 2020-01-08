---
layout: post
title: "Account Allocation"
category: "Accounting General Ledger" 
icon: "icon-money"
type: "data_access" comments: falsedescription: display the allocation tables specified in Fusion, along with the allocation breakdown for each by Branch/Department and the list of breakdown accounts specified in the setup form of the Allocation Table
---

---

This data object is used to display the allocation tables specified in Fusion,
along with the allocation breakdown for each by Branch/Department and the list
of breakdown accounts specified in the setup form of the Allocation Table.  It
also displays, for each allocation table, any GL account that it has been
associated with in the setup form of the given GL account, along with the branch
and/or department associated with that link.

This information comes from the Account Allocation and the Chart of Accounts
programs within the Fusion business system.

 <!-- SQL VIEW:  **vwAC_SSR_AccountAllocation**



 -->  <hr>Field Details...

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

## Accounting Chart of Accounts
---

This data object is used to show a listing of all general ledger chart of
accounts and their sub category structure down to 6 levels.

This information is found within the Chart of Accounts program within the Fusion
business system.

 <!-- SQL VIEW:  **vwAC_SSR_ChartofAccounts**



 -->  <hr>Field Details...

| **SQL Field Name**   | **Column Description**                                                                                                                                                                                                                                                                                                                                                                                                   |
|---|---|
| AccountingType       | This field displays the account type of the General Ledger Number.                                                                                                                                                                                                                                                                                                                                                       |
| AccountingCategory   | This field displays an accounting category assigned to a given account by a user.                                                                                                                                                                                                                                                                                                                                        |
| AddDate              | This field displays the date on which the given General Ledger number was added in the Business System.                                                                                                                                                                                                                                                                                                                  |
| AddUser              | This field displays the user name that added the record.                                                                                                                                                                                                                                                                                                                                                                 |
| ControlType          | This field displays the control type method assigned to the General Ledger Account. Options are: Not validated, Entity validation, or Validation list.                                                                                                                                                                                                                                                                   |
| Departmentalized     | This field displays whether or not a department is required when making postings to the General Ledger Account.                                                                                                                                                                                                                                                                                                          |
| DetailLevel          | This field displays how many levels down the G/L number is, based on the number of categories/sub categories above the G/L.  For example, say G/L 1100 resides under a category called Accounts Receivable, and the category Accounts Receivable was under the category of Assets.  G/L 1100 would then have a detail level of 3, as it is 3 levels deep, based on the categories/sub-categories under which it resides. |
| Account              | This field displays the general ledger account number associated with the debit or credit entry.                                                                                                                                                                                                                                                                                                                         |
| InActive             | This field displays whether or not a given general ledger account number is set to inactive.                                                                                                                                                                                                                                                                                                                             |
| LastUpdateDate       | This field displays the user name of the individual who made the update.                                                                                                                                                                                                                                                                                                                                                 |
| UpdateUser           | This field displays the user name of the individual who made the update.                                                                                                                                                                                                                                                                                                                                                 |
| Level1Category       | This field displays the top-most category under which the given G/L number falls.                                                                                                                                                                                                                                                                                                                                        |
| Level1SortOrder      | This field displays sort order of the level 1 category in relation to the other level 1 categories.                                                                                                                                                                                                                                                                                                                      |
| Level2Category       | This field displays the second level category assigned to the given G/L number. Note, that if the given G/L number does not have more than one parent category then the G/L number itself would be the level 2 category.                                                                                                                                                                                                 |
| Level2SortOrder      | This field displays sort order of the level 2 category in relation to the other level 2 categories found.                                                                                                                                                                                                                                                                                                                |
| Level3Category       | This field displays the third level category assigned to the given G/L number. Note, that if the given G/L number does not have 3 parent categories then the G/L number itself would be the level 3 category.                                                                                                                                                                                                            |
| Level3SortOrder      | This field displays sort order of the level 3 category in relation to the other level 3 categories found.                                                                                                                                                                                                                                                                                                                |
| Level4Category       | This field displays the fourth level category assigned to the given G/L number.  Note, that if the given G/L number does not have 4 parent categories then the G/L number itself would be the level 4 category.                                                                                                                                                                                                          |
| Level4SortOrder      | This field displays sort order of the level 4 category in relation to the other level 4 categories found.                                                                                                                                                                                                                                                                                                                |
| Level5Category       | This field displays the fifth level category assigned to the given G/L number. Note, that if the given G/L number does not have 5 parent categories then the G/L number itself would be the level 5 category.                                                                                                                                                                                                            |
| Level5SortOrder      | This field displays sort order of the level 5 category in relation to the other level 5 categories found.                                                                                                                                                                                                                                                                                                                |
| Level6Category       | This field displays the sixth level category assigned to the given G/L number. Note, that if the given G/L number does not have 5 parent categories then the G/L number itself would be the level 5 category.                                                                                                                                                                                                            |
| Level6SortOrder      | This field displays sort order of the level 6 category in relation to the other level 6 categories found.                                                                                                                                                                                                                                                                                                                |
| LongDescription      | This field displays the long description of a given General Ledger account.                                                                                                                                                                                                                                                                                                                                              |
| ShortDescription     | This field displays the short description of a given General Ledger account.                                                                                                                                                                                                                                                                                                                                             |
| StandardPresentation | This field displays either Debit or Credit based on the subcategory in which the given GL account resides.                                                                                                                                                                                                                                                                                                               |

## Accounting General Ledger Balance
---

This data object currently only pulls in the current year and the previous 2
years and next 2 years for a max total of 5 years of data.

 <!-- SQL VIEW:  **vwAC_SSR_GeneralLedgerBalance**



 -->  <hr>Field Details...

| **SQL Field Name**            | **Column Description**                                                                                                            |
|---|---|
| AccountType                   | This Field Displays the Account type of the General Ledger number.                                                                |
| AccountingCategory            | This Field Displays the Accounting Category Assigned to the General Ledger Number. Accounting Categories are user defined.        |
| AccountingPeriodBeginningDate | This Field Displays the date the accounting period began.                                                                         |
| AprilActivity                 | This field displays April's General Ledger Activity for the given branch, GL account, department, and fiscal year.                |
| AprilBudget                   | This field displays April's Budget Amount for the given branch, GL account, department, and fiscal year.                          |
| AprilPriorActivity            | This field displays April's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year.     |
| AugustActivity                | This field displays August's General Ledger Activity for the given branch, GL account, department, and fiscal year.               |
| AugustBudget                  | This field displays August's Budget Amount for the given branch, GL account, department, and fiscal year.                         |
| AugustPriorActivity           | This field displays August's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year.    |
| BalanceForward                | This field displays the balance forward of the GL account for the given branch and fiscal year.                                   |
| BalanceForwardPriorYear       | This field displays the prior year balance forward of the GL accoung for the given branch and fiscal year.                        |
| DecemberActivity              | This field displays December's General Ledger Activity for the given branch, GL account, department, and fiscal year.             |
| DecemberBudget                | This field displays December's Budget Amount for the given branch, GL account, department, and fiscal year.                       |
| DecemberPriorActivity         | This field displays December's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year.  |
| Department                    | This field displays the department we are displaying the data for.                                                                |
| DepartmentNumericCode         | This field displays the numeric code of the department we are displaying the data for.                                            |
| Description                   | This field displays the Long Description of a general ledger account number.                                                      |
| Division                      | This field displays the division the a branch is associated with.                                                                 |
| FebruaryActivity              | This field displays February's General Ledger Activity for the given branch, GL account, department, and fiscal year.             |
| FebruaryBudget                | This field displays February's Budget Amount for the given branch, GL account, department, and fiscal year.                       |
| FebruaryPriorActivity         | This field displays February's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year.  |
| FiscalYear                    | This field displays the fiscal year we are displaying the data for.                                                               |
| Branch                        | This field displays the branch we are displaying the data for.                                                                    |
| GLNumber                      | This field display a General Ledger account number.                                                                               |
| JanuaryActivity               | This field displays January's General Ledger Activity for the given branch, GL account, department, and fiscal year.              |
| JanuaryBudget                 | This field displays January's Budget Amount for the given branch, GL account, department, and fiscal year.                        |
| JanuaryPriorActivity          | This field displays January'sPrior year General Ledger Activity for the given branch, GL account, department, and fiscal year.    |
| JulyActivity                  | This field displays July's General Ledger Activity for the given branch, GL account, department, and fiscal year.                 |
| JulyBudget                    | This field displays July's Budget Amount for the given branch, GL account, department, and fiscal year.                           |
| JulyPriorActivity             | This field displays July's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year.      |
| JuneActivity                  | This field displays June's General Ledger Activity for the given branch, GL account, department, and fiscal year.                 |
| JuneBudget                    | This field displays June's Budget Amount for the given branch, GL account, department, and fiscal year.                           |
| JunePriorActivity             | This field displays June's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year.      |
| MarchActivity                 | This field displays March's General Ledger Activity for the given branch, GL account, department, and fiscal year.                |
| MarchBudget                   | This field displays March's Budget Amount for the given branch, GL account, department, and fiscal year.                          |
| MarchPriorActivity            | This field displays March's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year.     |
| MayActivity                   | This field displays May's General Ledger Activity for the given branch, GL account, department, and fiscal year.                  |
| MayBudget                     | This field displays May's Budget Amount for the given branch, GL account, department, and fiscal year.                            |
| MayPriorActivity              | This field displays May's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year.       |
| MTDActivity                   | This field displays the Month to Date activity of a branch/GL number/Department combination for the given fiscal year.            |
| MTDActivityPriorYear          | This field displays the Prior year Month to Date activity of a branch/GL number/department combination for the given fiscal year. |
| MTDActivityVariance           | This field displays the variance between MTD activity for the given fiscal year and the prior fiscal year.                        |
| MTDBudget                     | This field displays the Month to date budget figure of a branch/GL number combination/department for the given fiscal year.       |
| MTDBudgetVariance             | This field displays the variance between the MTD budget and the MTD activity of the given fiscal year.                            |
| NovemberActivity              | This field displays November's General Ledger Activity for the given branch, GL account, department, and fiscal year.             |
| NovemberBudget                | This field displays November's Budget Amount for the given branch, GL account, department, and fiscal year.                       |
| NovemberPriorActivity         | This field displays November's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year.  |
| OctoberActivity               | This field displays October's General Ledger Activity for the given branch, GL account, department, and fiscal year.              |
| OctoberBudget                 | This field displays October's Budget Amount for the given branch, GL account, department, and fiscal year.                        |
| OctoberPriorActivity          | This field displays October's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year.   |
| SeptemberActivity             | This field displays September's General Ledger Activity for the given branch, GL account, department, and fiscal year.            |
| SeptemberBudget               | This field displays September's Budget Amount for the given branch, GL account, department, and fiscal year.                      |
| SeptemberPriorActivity        | This field displays September's Prior year General Ledger Activity for the given branch, GL account, department, and fiscal year. |
| YTDActivity                   | This field displays the Year to Date activity of a branch/GL number/Department combination for the given fiscal year.             |
| YTDActivityPriorYear          | This field displays the Prior year YTD activity of a branch/GL number/department combination for the given fiscal year.           |
| YTDActivityVariance           | This field displays the variance between YTD activity for the given fiscal year and the prior fiscal year.                        |
| YTDBudget                     | This field displays the Year to date budget figure of a branch/GL number combination/department for the given fiscal year.        |
| YTDBudgetVariance             | This field displays the variance between the YTD budget and the YTD activity of the given fiscal year.                            |

## Accounting General Ledger Transaction
---

This data object is used to show all GL detail transactions in the Fusion
business system.

This information is found within the Accounting General Ledger Transaction
program within the Fusion business system.

 <!-- SQL VIEW:  **vwAC_SSR_GeneralLedgerTrans**



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
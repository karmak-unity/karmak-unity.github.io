---
layout: post
title: "General Ledger Balance"
category: "Accounting General Ledger" 
icon: "icon-money"
type: "data_access" comments: falsedescription: Display the current year, the previous 2 years and next 2 years for a max total of 5 years of data.
---

---
---

This data object currently only pulls in the current year and the previous 2 years and next 2 years for a max total of 5 years of data.

#### URL
```
/frw/GeneralLedgerBalance
```
 <hr>Field Details...

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
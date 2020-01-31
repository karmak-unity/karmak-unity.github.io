---
layout: post
title: "Check Register"
category: "Accounting Other" 
icon: "icon-credit-card1"
type: "data_access" comments: falsedescription:  Return all checks that have been issued in the Fusion Business System
---

---

This data object is used to return all checks that have been issued in the
Fusion Business System.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**  | **Column Description**                                                                                                                 |
|---|---|
| AddDate             | This field displays the date on which the check was added.                                                                             |
| AddUser             | This field displays the user name of the individual who added the given check.                                                         |
| Address1            | This field displays the address line 1 of the check.                                                                                   |
| Address2            | This field displays the address line 2 of the check.                                                                                   |
| APVendor            | If present, this field displays the Accounts Payable vendor to which the check was issued.                                             |
| Bank                | This field displays the bank out of which the given check was issued.                                                                  |
| CheckAmount         | This field displays the amount for which the given check was issued.                                                                   |
| CheckDate           | This field displays the date on which the given check was issued.                                                                      |
| CheckNumber         | This field displays the check number assigned to the given check.                                                                      |
| CheckSource         | This field displays the type of the given check (A/P check, G/L check, notes payable check, refund check).                             |
| CheckStatus         | This field displays Voided if the given check has been voided, or Not Voided if the given check has not been voided.                   |
| City                | This field displays the city of the check.                                                                                             |
| Cleared             | This field displays whether or not the given check has been marked as cleared.                                                         |
| ClearedDate         | This field displays the date on which the given check was cleared.                                                                     |
| ClearedStatus       | This field displays Cleared if the given check has been marked as cleared, or Not Cleared if the given check is not marked as cleared. |
| CustomerNumber      | If present, this field displays the customer number of the customer to which the check was issued.                                     |
| LastUpdateDate      | This field displays the date on which the check was last updated.                                                                      |
| LastUpdateUser      | This field displays the user name of the individual who last updated the given check.                                                  |
| Lender              | If present, this field displays the lender to which the check was issued.                                                              |
| PayeeName           | This field displays the payee name to which the check was issued.                                                                      |
| PostalCode          | This field displays the postal code of the check.                                                                                      |
| PostingBranch       | This field displays the branch that posted the given check.                                                                            |
| PostingPeriod       | This field displays the accounting posting period for which the given check was posted.                                                |
| PostingSequence     | This field displays the accounting transaction posting sequence of the given check.                                                    |
| IsReconciled        | This field displays whether or not the given check has been reconciled in  Account Reconciliation.                                     |
| Region              | This field displays the region of the check.                                                                                           |
| VoidDate            | This field displays the date on which the given check was voided.                                                                      |
| VoidDescription     | This field displays the voided description for the given check.                                                                        |
| VoidPeriod          | This field displays the accounting posting period into which the given check was voided.                                               |
| VoidPostingSequence | This field displays the voided posting sequence for the given check.                                                                   |
| VoidUser            | This field displays the user name of the individual who voided the given check.                                                        |
| IsVoided            | This field displays whether or not the given check has been voided.                                                                    |
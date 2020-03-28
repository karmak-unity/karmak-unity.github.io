---
layout: post
title: "Accounts Payable General Ledger Detail"
category: "Accounts Payable" 
icon: "icon-shopping-bag"
type: "data_access" 
comments: false
description: Access to all general ledger detail of accounts payable invoices.
---
---

This data object is used to display general ledger detail of accounts payable invoices.

This information is located in Accounts Payable Invoice Entry and General Ledger Transactions within the Fusion business system.


#### URL 
```
/frw/APGLDetail
``` 
 <hr>
Field Details...

| **SQL Field Name**         | **Column Description**                                                                                |
|---|---|
| AllocationName             | This field displays the allocation table associated with the AP detail line item.                     |
| APInvoice                  | This field displays a given Accounts Payable Invoice.                                                 |
| ControlValue               | This field displays the control value of the detail line item.                                        |
| CreditAmount               | This field Displays the Credit amount of the AP GL detail item.                                       |
| DebitAmount                | This field Displays the Debit amount of the AP GL detail item.                                        |
| Department                 | This field displays the department associated with an AP Invoice Detail item.                         |
| GLAccount                  | This field displays the general ledger account number associated with the general ledger transaction. |
| GLBranch                   | This field displays the Branch the AP GL item is posting to.                                          |
| InvoiceAmount              | This field displays the amount due for a given A/P invoice.                                           |
| InvoiceDate                | This field displays the invoice date for a given A/P Invoice.                                         |
| OverridePostingDescription | This field displays the override description for a given transaction.                                 |
| PostingBranch              | This field displays the branch that posted the AP GL detail item.                                     |
| PostingDescription         | This field displays a posting description for an Accounts Payable invoice.                            |
| Vendor                     | This field displays the vendor attached to a given A/P invoice.                                       |
| VendorName                 | This field displays the name of the vendor attached to a given A/P invoice.                           |
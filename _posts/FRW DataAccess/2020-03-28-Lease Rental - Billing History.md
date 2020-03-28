---
layout: post
title: "Lease Rental Billing History"
category: "Lease / Rental" 
icon: "icon-user-plus1"
type: "data_access" 
comments: false
description: Display the overall totals and information about a given LR invoice.
---

---
---

This data object is used to display the overall totals and information about a given LR invoice.

This information can be found in the LR Billing History application in the Fusion business system.

 
#### URL 
```
/frw/LRBillingHistory
``` 

<hr>
Field Details...

| **SQL Field Name**   | **Column Description**                                                                                           |
|---|---|
| AddDate              | This field displays the date on which the given LR invoice was added to the system.                              |
| AddUser              | This field displays the user name of the user who added the given LR invoice to the system.                      |
| Branch               | This field displays the branch in which the given LR invoice was created.                                        |
| CompanyName          | This field displays the company name of the customer associated with the given LR invoice.                       |
| ContractNumber       | This field displays the contract number of the LR contract on the given LR invoice.                              |
| ContractSalesperson  | This field displays the salesperson listed on the given LR contract.                                             |
| CustomerKey          | This field displays the identifying number of the customer associated with the given LR invoice.                 |
| Department           | This field displays the department in which the given LR invoice was created.                                    |
| Division             | This field displays the division in which the given LR invoice was created.                                      |
| DueDate              | This field displays the date on which the given LR invoice is due to be paid.                                    |
| FixedBillingGroup    | This field displays the billing group used for the fixed charges on the given LR invoice.                        |
| InvoiceDate          | This field displays the date on which the given LR invoice was invoiced.                                         |
| InvoiceNumber        | This field displays the invoice number of the given LR invoice.                                                  |
| LastUpdateDate       | This field displays the date on which the given LR invoice was last updated in the system.                       |
| LastUpdateUser       | This field displays the user name of the user who last updated the given LR invoice in the system.               |
| PaymentMethod        | This field displays the payment method by which the customer will be paying the given LR invoice.                |
| PaymentTerms         | This field displays the payment terms which apply to the customer regarding the payment of the given LR invoice. |
| PostingPeriod        | This field displays the period in which the given LR invoice was posted.                                         |
| Subtotal             | This field displays the total amount of the fixed, variable, and miscellaneous charges on the given LR invoice.  |
| TotalFixed           | This field displays the total amount of the fixed charges on the given LR invoice.                               |
| TotalInvoice         | This field displays the total amount of the given LR invoice, including all charges and taxes.                   |
| TotalMisc            | This field displays the total amount of the miscellaneous charges on the given LR invoice.                       |
| TotalTax             | This field displays the total amount of taxes charged on the given LR invoice.                                   |
| TotalVariable        | This field displays the total amount of the variable charges on the given LR invoice.                            |
| VariableBillingGroup | This field displays the billing group used for the variable charges on the given LR invoice.                     |
| IsVoided             | This field displays whether the given LR invoice has been voided.                                                |



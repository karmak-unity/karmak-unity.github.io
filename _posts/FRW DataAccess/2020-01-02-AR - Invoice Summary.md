---
layout: post
title: "Invoice Sales Summary"
category: "Account Recievables" 
icon: "icon-credit-card1"
type: "data_access" comments: falsedescription: Displays the summarys of all invoices and/or orders, parts orders, invoices, deals, contracts.
---

---
---
This data object displays all invoiced and/or voided repair orders, parts orders, LR contracts, finance charges, deals, fuel invoices, and adjustment invoices, regardless of whether they have been paid in full.

This information can be found in the respective invoicing applications in the Fusion business system.

 #### URL 
```
/frw/InvoiceSalesSummary
```  <hr>Field Details...

| **SQL Field Name**               | **Column Description**                                                                                                           |
|---|---|
| AddDate                          | This field displays the date on which the given invoice was created.                                                             |
| AddUser                          | This field displays the username of the user that originally added the open order, which has since been invoiced, to the system. |
| AverageCostGrossProfit           | This field displays the gross profit of the given invoice, based on the average cost of the items on the invoice.                |
| AverageCostGrossProfitMargin     | This field displays the gross profit margin of the given invoice, based on the average cost of the items on the invoice.         |
| BillingCompanyName               | This field displays the company name of the billing customer on the given invoice.                                               |
| BillingCustomer                  | This field displays the customer number of the billing customer on the given invoice.                                            |
| BillingCustomerAddress1          | This field displays the first line of the Bill To address for the billing customer on the given invoice.                         |
| BillingCustomerAddress2          | This field displays the second line of the Bill To address for the billing customer on the given invoice.                        |
| BillingCustomerCity              | This field displays the city of the Bill To address for the billing customer on the given invoice.                               |
| BillingCustomerCounty            | This field displays the county of the Bill To address for the billing customer on the given invoice.                             |
| BillingCustomerPostalCode        | This field displays the postal code of the Bill To address for the billing customer on the given invoice.                        |
| BillingCustomerRegion            | This field displays the region or state of the Bill To address for the billing customer on the given invoice.                    |
| CompanyName                      | This field displays the company name of the customer who ordered the given invoice.                                              |
| Customer                         | This field displays the customer number of the customer who ordered the given invoice.                                           |
| CustomerPO                       | This field displays the customer PO number on the given invoice.                                                                 |
| Department                       | This field displays the department in which the invoice was created.                                                             |
| Division                         | This field displays the division in which the invoice was created.                                                               |
| Branch                           | This field displays the branch in which the invoice was created.                                                                 |
| InvoiceDate                      | This field displays the date on which the given item was invoiced.                                                               |
| InvoiceNumber                    | This field displays the invoice number of the given invoice.                                                                     |
| InvoiceSubTotal                  | This field displays the total of the given invoice, excluding taxes.                                                             |
| InvoiceTaxTotal                  | This field displays the total taxes charged on the given invoice.                                                                |
| InvoiceTotal                     | This field displays the total of the given invoice, including taxes.                                                             |
| OrderType                        | This field displays the type of the given invoice, based on the module and/or application in Fusion in which it was created.     |
| InvoiceUser                      | This field displays the username of the user that invoiced the given order.                                                      |
| LastUpdate                       | This field displays the date on which the given invoice was last updated.                                                        |
| UpdateUser                       | This field displays the user name of the user that last updated the invoice.                                                     |
| IsLocal                          | This field displays whether the given invoice should have the local sales tax applied to it, if the invoice is taxable.          |
| OrderCustomerAddress1            | This field displays the first line of the Ship To address for the customer who ordered the given invoice.                        |
| OrderCustomerAddress2            | This field displays the second line of the Ship To address for the customer who ordered the given invoice.                       |
| OrderCustomerCity                | This field displays the city of the Ship To address for the customer who ordered the given invoice.                              |
| OrderCustomerCounty              | This field displays the county of the Ship To address for the customer who ordered the given invoice.                            |
| OrderCustomerPostalCode          | This field displays the postal code of the Ship To address for the customer who ordered the given invoice.                       |
| OrderCustomerRegion              | This field displays the region or state of the Ship To address for the customer who ordered the given invoice.                   |
| OrderNumber                      | This field displays the order number of the original item that was invoiced.                                                     |
| PaymentMethod                    | This field displays the payment method by which the customer will pay the invoice.                                               |
| ReplacementCostGrossProfit       | This field displays the gross profit of the given invoice, based on the replacement cost of the items on the invoice.            |
| ReplacementCostGrossProfitMargin | This field displays the gross profit margin of the given invoice, based on the replacement cost of the items on the invoice.     |
| Salesperson                      | This field displays the outside salesperson associated with the sale to the given customer via the given invoice.                |
| TotalAverageCost                 | This field displays the total average cost of all the items on the given invoice.                                                |
| TotalReplacementCost             | This field displays the total replacement cost of all the items on the given invoice.                                            |
| IsVoidedInvoice                  | This field displays whether the given invoice has been voided.                                                                   |
---
layout: post
title: "Salesperson Commission"
category: "Accounting Other" 
icon: "icon-credit-card1"
type: "data_access" comments: falsedescription: Access to the parts and service salesperson commission records 
---

---

This data object displays parts and service salesperson commission records as
seen in the Salesperson Commission Display application in Fusion.

 <!-- SQL VIEW:  **vwAC_SSR_SalesPersonCommission**



 -->  <hr>Field Details...

| **SQL Field Name**   | **Column Description**                                                                                                             |
|---|---|
| Branch               | This field displays the branch associated with the invoice record for the commission detail item.                                  |
| Commission           | This field displays the commission the salesperson received for the line item.                                                     |
| Commission Rate      | This field displays the commission rate for the salesperson.                                                                       |
| CommissionTable      | This field displays the commission table applied to the user branch department record that determines the commission.              |
| Customer             | This field displays the customer number associated with the invoice record.                                                        |
| Department           | This field displays the department associated with the invoice record for the commission detail item.                              |
| ExtendedCost         | This field displays the extended cost of the item sold on the invoice.                                                             |
| ExtendedPrice        | This field displays the extended price of the item sold on the invoice.                                                            |
| GrossProfit          | This field displays the gross profit of the item sold.                                                                             |
| GrossProfitMargin    | This field displays the gross profit margin of the item sold.                                                                      |
| InvoiceDate          | This field displays the invoice date of the invoice assocaited with commission detail item.                                        |
| InvoiceDateandTime   | This field displays the invoice date and time of the invoice assocaited with commission detail item.                               |
| InvoiceNumber        | This field displays the invoice number associated with the commission detail item.                                                 |
| Item                 | This field displays the item that was sold.                                                                                        |
| IsOutsideSalesperson | This field displays Yes, if the salesperson associated with the detail is an outside salesperson, or No if the salesperson is not. |
| Quantity             | This field displays the quantity of the item sold.                                                                                 |
| Salesperson          | This field displays the Salespersons username associated with the commission detail record.                                        |
| SalespersonName      | This field displays the Salespersons first name and last name.                                                                     |
| IsVoided             | If the record is for a voided invoice, this field is set to Yes. If not, this field is set to No.                                  |

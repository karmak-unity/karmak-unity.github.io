---
layout: post
title: "Parts Customer Purchase and Return"
category: "Parts"
icon: "icon-gear"
type: "data_access" comments: falsedescription: Customer Core Right to Return program within the Fusion business system
---

---
---
### Customer Core Right To Return
---

This data object is used to show a list of customer core right to return
records.

This information is pulled from the Customer Core Right to Return program within
the Fusion business system.

 <!-- SQL VIEW:  **vwIN_SSR_CustomerCoreRighttoReturn**



 -->  <hr>Field Details...

| **SQL Field Name** | **Column Description**                                                                          |
|---|---|
| AddDate            | This field displays the date and time on which the record was added.                            |
| AddUser            | This field displays the user name that added the record.                                        |
| Branch             | This field displays the branch associated with a customer core right to return.                 |
| CompanyName        | This field displays the company name of the customer associated with the order.                 |
| CustomerNumber     | This field displays the identifying number attached to a customer.                              |
| ExpirationDate     | This field displays the date on which a customer's right to return the given core expires.      |
| InvoiceDate        | This field displays the invoice date for the given invoice.                                     |
| InvoiceNumber      | This field displays the invoice number for the given invoice.                                   |
| LastUpdate         | This field displays the date and time on which the record was last updated.                     |
| UpdateUser         | This field displays the user name of the individual who made the last update.                   |
| MaximumPrice       | This field displays the maximum price for a given part.                                         |
| IsNoCharge         | This field displays whether or not the part was sold as no charge to the customer on the order. |
| PartDescription    | This field displays the description of the given part.                                          |
| PartNumber         | This field displays the part number of the given part.                                          |
| SalesOrderNumber   | This field displays the number attached to a sales order.                                       |
| Quantity           | This field displays the quantity requested for a given part.                                    |
| RepairOrderNumber  | This field displays the number attached to a repair order.                                      |
| SoldDate           | This field displays the date and time on which a core was sold.                                 |
| Supplier           | This field displays the supplier of the part.                                                   |

---
---
### Parts Customer Purchases And Returns
---

This data object is used to show a list of parts and miscellaneous charges from
invoiced parts orders, repair orders, or 3rd party converted data for a
customer.

This information is from the Customer Purchases/Returns program within the
Fusion business system.

 <!-- SQL VIEW:  **vwIN_SSR_CustomerPurchasesandReturns**



 -->  <hr>Field Details...

| **SQL Field Name**             | **Column Description**                                                                                                                                                     |
|---|---|
| AddDate                        | This field displays the date on which the record was added.                                                                                                                |
| AddUser                        | This field displays the user name that added the record.                                                                                                                   |
| AverageCost                    | This field displays the average cost of the given item at the time the item was purchased.                                                                                 |
| Branch                         | This field displays the branch associated with the purchase.                                                                                                               |
| CompanyName                    | This field displays the company name of the customer associated with the purchase/return.                                                                                  |
| IsCore                         | This field displays whether or not the given detail item is a core.                                                                                                        |
| Customer                       | This field displays the customer attached to an invoiced sale.                                                                                                             |
| Department                     | This field displays the department associated with the given order.                                                                                                        |
| Division                       | This field displays the company division in which the given order was created.                                                                                             |
| ExtendedPrice                  | This field shows the extended price of the given detail item.                                                                                                              |
| InvoiceDate                    | This field displays the date on which the order was invoiced.                                                                                                              |
| InvoiceNumber                  | This field displays the invoice number of the given invoice.                                                                                                               |
| ItemNumber                     | This field displays the identifying name of the given detail item (part number for parts, charge name for miscellaneous charges).                                          |
| ItemDescription                | This field displays the description of the given detail item.                                                                                                              |
| ItemType                       | This field displays the type of the given item. (Part for Parts, EXC for Exchange parts, RET for Return Cores, INH for Inherent Cores, and Misc for Miscelaneous charges). |
| LastUpdate                     | This field displays the date on which the item was last updated on the order.                                                                                              |
| UpdateUser                     | This field displays the user name of the individual who made the update.                                                                                                   |
| IsMiscCharge                   | This field displays whether or not the given detail item is a miscellaneous charge.                                                                                        |
| MiscellaneousCharge            | This field displays the name of the given miscellaneous charge.                                                                                                            |
| MiscellaneousChargeDescription | This field displays the description of the given miscellaneous charge.                                                                                                     |
| OrderType                      | This field displays what type of order the part was sold on or Converted Data if the record was converted in to the system.                                                |
| PartDescription                | For parts, this field will display the description of the part.                                                                                                            |
| PartNumber                     | For parts, this field will display the part number of the part.                                                                                                            |
| PartsOrderActionType           | This field displays the Action Type associated with the part sale and will only by populated for part records that were not converted into the system from another source. |
| Price                          | This field displays the selling price of the given item.                                                                                                                   |
| CustomerPurchaseOrder          | This field displays the purchase order number associated with the given order.                                                                                             |
| Quantity                       | This field displays the quantity purchased for the given item.                                                                                                             |
| IsQCInvoiceNumber              | This field displays if the parts invoice was created via Quick Credit.                                                                                                     |
| IsRepairOrder                  | This field displays whether or not the given detail item is from a repair order.                                                                                           |
| ReplacementCost                | This field displays the replacement cost of the givem item at the time the item was purchased.                                                                             |
| Supplier                       | This field displays the supplier of the given item.                                                                                                                        |
| IsVoided                       | This field displays whether or not the given order has been voided.                                                                                                        |
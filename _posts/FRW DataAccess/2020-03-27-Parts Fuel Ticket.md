---
layout: post
title: "Parts Fuel Ticket and Detail"
category: "Parts"
icon: "icon-gear"
type: "data_access" 
comments: false
description: Access to display fuel ticket summary information for open and invoiced fuel tickets, as well as fuel tickets that are included on LR Contract invoices.
---


---
---
### Parts Fuel Ticket
---

This data object is used to display fuel ticket summary information for open and invoiced fuel tickets, as well as fuel tickets that are included on LR Contract invoices.

This information comes from the Fuel Ticket Entry, Fuel Ticket Billing, and LR Billing programs in the Fusion business system.

#### URL 
```
/frw/FuelTicket
``` 

<hr>
Field Details...

| **SQL Field Name** | **Column Description**                                                                                                                                                                                                                        |
|---|---|
| AddDate            | This field displays the date on which the fuel ticket was created.                                                                                                                                                                            |
| AddUser            | This field displays the user name of the user that created the fuel ticket.                                                                                                                                                                   |
| Branch             | This field displays the branch associated with the fuel ticket.                                                                                                                                                                               |
| CompanyName        | This field displays the company name of the customer associated with the fuel ticket.                                                                                                                                                         |
| ContractNumber     | This field displays the contract number of the LR Contract the fuel ticket is associated with.                                                                                                                                                |
| CustomerNumber     | This field displays the unique number associated with the customer in Fusion.                                                                                                                                                                 |
| Department         | This field displays the department associated with the fuel ticket.                                                                                                                                                                           |
| FuelCharges        | This field displays the total fuel charges associated with the fuel ticket.                                                                                                                                                                   |
| FuelTicketStatus   | This field displays Open for open fuel tickets, Invoiced for fuel tickets that have been invoiced, or Voided for fuel tickets on LR Contract invoices that have been voided.                                                                  |
| InvoiceDate        | This field displays the invoice date of the fuel ticket that has been invoiced in Fuel Ticket Billing or the invoice date or void date of the LR Contract that has been invoiced or voided with the given fuel ticket attached, respectively. |
| InvoiceNumber      | This field displays the invoice number of the fuel ticket that has been invoiced in Fuel Ticket Billing or the invoice number of the LR Contract that has been invoiced and/or voided with the given fuel ticket attached.                    |
| LastUpdate         | This field displays the date on which the fuel ticket was last updated.                                                                                                                                                                       |
| UpdateUser         | This field displays the user name of the user that last updated the fuel ticket.                                                                                                                                                              |
| IsLRInvoice        | This field displays whether or not the fuel ticket has been associated with an LR Contract invoice.                                                                                                                                           |
| MeterReading       | This field displays the meter reading for a given unit at the time the fuel ticket occurred.                                                                                                                                                  |
| MiscCharges        | This field displays the total miscellaneous charges associated with the fuel ticket.                                                                                                                                                          |
| PaymentMethod      | This field displays the payment method, defined by the user, associated with the fuel ticket.                                                                                                                                                 |
| PurchaseOrder      | This field displays the purchase order number associated with the fuel ticket.                                                                                                                                                                |
| Source             | This field displays whether the fuel ticket was imported from Fuel Master or manually entered through Fuel Ticket Entry.                                                                                                                      |
| TaxBody            | This field displays the tax body associated with the fuel ticket.                                                                                                                                                                             |
| TaxStatus          | This field displays the tax status of the customer associated with the fuel ticket.                                                                                                                                                           |
| TaxTotal           | This field displays the total taxes charged on the charges associated with the fuel ticket.                                                                                                                                                   |
| TicketDate         | This field displays the date the fuel transaction took place.                                                                                                                                                                                 |
| TicketNumber       | This field displays the ticket number of the fuel ticket.                                                                                                                                                                                     |
| TicketTotal        | This field displays the total of the fuel charges, misc charges, and taxes associated with the fuel ticket.                                                                                                                                   |
| UnitNumber         | This field displays the unit number of the unit associated with the fuel ticket.                                                                                                                                                              |
| IsVoided           | This field displays whether or not the LR Contract invoice that the fuel ticket is associated with has been voided.                                                                                                                           |

---
---
### Parts Fuel Ticket Detail
---

This data object is used to display all of the detail line items from Fuel
Tickets created and/or invoiced (and/or voided for Fuel Tickets on L/R invoices)
in the Fusion business system.

This information can be found in the Fuel Ticket Entry program in the Fusion
business system.

 
#### URL 
```
/frw/FuelTicketDetail
``` 
 <hr>
Field Details...

| **SQL Field Name**  | **Column Description**                                                                                                                                                                                                                        |
|---|---|
| AddDate             | This field displays the date on which the fuel or miscellaneous charge was added to the fuel ticket.                                                                                                                                          |
| AddUser             | This field displays the user name of the user that added the fuel or miscellaneous charge to the fuel ticket.                                                                                                                                 |
| AverageCost         | This field displays the average cost of the given fuel per one unit at the time it was added to the fuel ticket.                                                                                                                              |
| Branch              | This field displays the branch associated with the fuel ticket.                                                                                                                                                                               |
| Cost                | This field displays the cost of the given fuel or miscellaneous charge per one unit.                                                                                                                                                          |
| Department          | This field displays the department associated with the fuel ticket.                                                                                                                                                                           |
| Description         | This field displays the description of the given fuel or miscellaneous charge.                                                                                                                                                                |
| Division            | This field displays the division associated with the fuel ticket.                                                                                                                                                                             |
| ExtendedAverageCost | This field displays the total average cost (average cost \* quantity) of the given fuel charge.                                                                                                                                               |
| ExtendedCost        | This field displays the total cost (cost \* quantity) of the given fuel or miscellaneous charge.                                                                                                                                              |
| ExtendedMarketRate  | This field displays the total market rate (market rate \* quantity) of the given fuel charge.                                                                                                                                                 |
| ExtendedPrice       | This field displays the total price (price \* quantity) of the given fuel or miscellaneous charge.                                                                                                                                            |
| InvoiceDate         | This field displays the invoice date of the fuel ticket that has been invoiced in Fuel Ticket Billing or the invoice date or void date of the LR Contract that has been invoiced or voided with the given fuel ticket attached, respectively. |
| InvoiceNumber       | This field displays the invoice number of the fuel ticket that has been invoiced in Fuel Ticket Billing or the invoice number of the LR Contract that has been invoiced and/or voided with the given fuel ticket attached.                    |
| Item                | This field displays the short, identifying name of the given fuel or miscellaneous charge.                                                                                                                                                    |
| ItemType            | This field displays Misc for a miscellaneous charge or Fuel for a fuel charge, to reflect the type of the charge on the given fuel ticket.                                                                                                    |
| LastUpdate          | This field displays the date on which the fuel or miscellaneous charge was last updated on the given fuel ticket.                                                                                                                             |
| UpdateUser          | This field displays the user name of the user that last updated the fuel or miscellaneous charge on the given fuel ticket.                                                                                                                    |
| IsLRInvoice         | This field displays whether or not the fuel ticket has been associated with an LR Contract invoice.                                                                                                                                           |
| MarketRate          | This field displays the market rate of the given fuel per one unit at the time it was added to the fuel ticket.                                                                                                                               |
| OrderStatus         | This field displays ''Open'' for open fuel tickets, ''Invoiced'' for fuel tickets that have been invoiced, or ''Voided'' for fuel tickets on LR Contract invoices that have been voided.                                                      |
| Price               | This field displays the price of the given fuel or miscellaneous charge for the customer per one unit.                                                                                                                                        |
| Pump                | This field displays the pump from which the given fuel comes.                                                                                                                                                                                 |
| Quantity            | This field displays the number of units of the given fuel or miscellaneous charge added to the fuel ticket.                                                                                                                                   |
| StockNumber         | This field displays the stock number associated with the unit listed on the fuel ticket.                                                                                                                                                      |
| Tank                | This field displays the tank in which the given fuel is located.                                                                                                                                                                              |
| TicketDate          | This field displays the date the fuel transaction took place.                                                                                                                                                                                 |
| TicketNumber        | This field displays the ticket number of the fuel ticket.                                                                                                                                                                                     |
| UnitNumber          | This field displays the unit number listed on the fuel ticket.                                                                                                                                                                                |
| IsVoided            | This field displays whether or not the LR Contract invoice that the fuel ticket is associated with has been voided.                                                                                                                           |
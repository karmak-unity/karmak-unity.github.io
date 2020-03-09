---
layout: post
title: "Parts Order"
category: "Parts" 
icon: "icon-gear"
type: "data_access" comments: falsedescription: Access to Parts Order within Fusion
---

---
---


This data object is used to display all parts order header records.

This information is located within the Parts Order program in the Fusion
business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**               | **Column Description**                                                                                                                                                                                                                                                             |
|---|---|
| AddUser                          | This field displays the username of the user who added the given parts order to Fusion or, for invoiced parts orders, displays the username of the user who added the original parts order, pre-invoicing, to Fusion. Note that at this point this field is not exposed in Fusion. |
| AverageCost                      | This field displays the total average cost of the given parts order.                                                                                                                                                                                                               |
| AverageCostGrossProfit           | This field displays the gross profit of the given parts order based on average cost.                                                                                                                                                                                               |
| AverageCostGrossProfitMargin     | This field displays the gross profit margin of the given parts order based on average cost.                                                                                                                                                                                        |
| BillingCompanyName               | This field displays the name of a billing company for a parts order.                                                                                                                                                                                                               |
| BillingContactName               | This field displays the contact name for a billing customer.                                                                                                                                                                                                                       |
| BillingCustomerAccountStatus     | This field displays the status of an account for a billing customer.                                                                                                                                                                                                               |
| BillingCustomerNumber            | This field displays the Customer Number of a billing customer for a parts order.                                                                                                                                                                                                   |
| BillingHomePhone                 | This field displays the billing customer's home phone number.                                                                                                                                                                                                                      |
| BillingWorkPhone                 | This field displays the billing customer's work phone number.                                                                                                                                                                                                                      |
| Branch                           | This field displays the branch associated with the parts order.                                                                                                                                                                                                                    |
| CanadianTaxID                    | This field displays the Canadian tax ID listed on the customer form or entered at the time of invoicing.                                                                                                                                                                           |
| CompanyName                      | This field displays the company name associated with the customer on the parts order.                                                                                                                                                                                              |
| ContactHomePhone                 | This field displays the contact's home phone number.                                                                                                                                                                                                                               |
| ContactName                      | This field displays the contact's name.                                                                                                                                                                                                                                            |
| ContactWorkPhone                 | This field displays the contact's work phone number.                                                                                                                                                                                                                               |
| CreationDate                     | This field displays the date on which a parts order was created.                                                                                                                                                                                                                   |
| CustomerAccountStatus            | This field displays the status of a customer account for a parts order.                                                                                                                                                                                                            |
| CustomerNumber                   | This field displays the identifying number attached to a customer.                                                                                                                                                                                                                 |
| CustomerPO                       | This field displays the customer purchase order associated with an invoiced sale.                                                                                                                                                                                                  |
| DeliveryDate                     | This field displays the delivery date assigned to the given parts order.                                                                                                                                                                                                           |
| Department                       | This field displays the department associated with a parts order.                                                                                                                                                                                                                  |
| Division                         | This field displays the company division associated with the given parts order.                                                                                                                                                                                                    |
| InvoiceDate                      | This field displays the invoice date of the given parts order.                                                                                                                                                                                                                     |
| InvoiceNumber                    | If present, this field displays the invoice number of the parts order.                                                                                                                                                                                                             |
| InvoiceUser                      | This field displays the username of the user who invoiced or voided the given invoiced or voided parts order.                                                                                                                                                                      |
| ItemsReadyforPickup              | This field displays whether or not items on a parts order are ready for pickup.                                                                                                                                                                                                    |
| LastUpdate                       | This field displays the date the parts order Header was last updated.  Note, at this point in time this field is not exposed in Fusion.                                                                                                                                            |
| UpdateUser                       | This field displays the username of the user who last updated the header of the given parts order or, for invoiced parts orders, displays the username of the user who last updated the given invoice. Note that at this point this field is not exposed in Fusion.                |
| IsLocal                          | This field displays whether or not a given parts order is local.                                                                                                                                                                                                                   |
| LPO                              | This field displays the local purchase order number tied to the parts order if one exists.                                                                                                                                                                                         |
| OrderStatus                      | This field displays the status of an order on a miscellaneous purchase order.                                                                                                                                                                                                      |
| OrderSubtotal                    | This field displays the order total not including tax.                                                                                                                                                                                                                             |
| OrderTotal                       | This field displays the total amount for a parts order.                                                                                                                                                                                                                            |
| OutsidePartsSalesperson          | This field displays the outside parts salesperson attached to a given parts order.                                                                                                                                                                                                 |
| PartsAccounting                  | This field displays the alternate parts accounting if any has been selected.                                                                                                                                                                                                       |
| PartsOrderNumber                 | This field displays the number attached to a given parts order.                                                                                                                                                                                                                    |
| PaymentMethod                    | This field displays the payment method of the given parts order.                                                                                                                                                                                                                   |
| PickupDeliveryMethod             | This field displays how a parts order will reach the customer.                                                                                                                                                                                                                     |
| QuebecTaxID                      | This field displays the Quebec tax ID listed on the customer form or entered at the time of invoicing.                                                                                                                                                                             |
| ReplacementCost                  | This field displays the total replacement cost of the given parts order.                                                                                                                                                                                                           |
| ReplacementCostGrossProfit       | This field displays the gross profit of the given parts order based on replacement cost.                                                                                                                                                                                           |
| ReplacementCostGrossProfitMargin | This field displays the gross profit margin of the given parts order based on replacement cost.                                                                                                                                                                                    |
| SalesTaxTotal                    | This field displays the total amount of sales tax charged for a parts order.                                                                                                                                                                                                       |
| SalesTerritory                   | This field displays the sales territory associated with a part order.                                                                                                                                                                                                              |
| ShipToAddress1                   | This field displays line one of the customer's shipping address, found on the address entry tab of parts order.                                                                                                                                                                    |
| ShipToAddress2                   | This field displays line two of the customer's shipping address, found on the address entry tab of parts order.                                                                                                                                                                    |
| ShipToCity                       | This field displays the customer's shipping city, found on the address entry tab of parts order.                                                                                                                                                                                   |
| ShipToCustomerName               | This field displays the ship-to company name, found on the address entry tab of parts order.                                                                                                                                                                                       |
| ShipToEmail                      | This field displays the ship-to email address, found on the address entry tab of parts order.                                                                                                                                                                                      |
| ShipToFax                        | This field displays the ship-to fax number, found on the address entry tab of parts order.                                                                                                                                                                                         |
| ShipToOfficePhone                | This field displays the ship-to office phone number, found on the address entry tab of parts order.                                                                                                                                                                                |
| ShipToPostalCode                 | This field displays the customer's shipping postal code, found on the address entry tab of parts order.                                                                                                                                                                            |
| ShipToRegion                     | This field displays the customer's shipping region, found on the address entry tab of parts order.                                                                                                                                                                                 |
| ShipToShopPhone                  | This field displays the ship-to shop phone, found on the address entry tab of parts order.                                                                                                                                                                                         |
| Source                           | This field displays the source from which the given parts order originated.  Valid sources are: Parts Counter, Business Online, WHI, Channel Advisor, EDI, and DTNA.                                                                                                               |
| TaxBody                          | This field displays the tax body associated with a customer address.                                                                                                                                                                                                               |
| TaxCode                          | This field displays the tax code assigned to a customer.                                                                                                                                                                                                                           |
| Territory                        | This field displays the territory field found on the billing customer tab of the parts order.                                                                                                                                                                                      |
| TrackingNumber                   | This field displays the tracking number entered in the Tracking Number field in the header of the parts order.                                                                                                                                                                     |
| IsVoided                         | This field display wether the the given parts order has been voided or not.                                                                                                                                                                                                        |

---
---
### Parts Order Detail
---

This data object is used to display all of the detail records on open, invoiced,
and/or voided parts orders.

This information is located in the Parts Order application in the Fusion
business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**      | **Column Description**                                                                                                                                         |
|---|---|
| AddDate                 | This field displays the date on which the given part was added to the parts order.                                                                             |
| AddUser                 | This field displays the username of the user who added the given parts order detail item to the parts order.                                                   |
| AverageCost             | This field displays the average cost of the given part.                                                                                                        |
| BackOrderPriority       | This field displays the priority flag assigned to the given part on backorder when it was added to the parts order.                                            |
| IsBackorder             | This field displays whether the given part was backordered.                                                                                                    |
| BinLocation             | This field displays the Bin Location that the user selected when adding the part to the parts order, it will defualt to the part's primary bin location.       |
| Branch                  | This field displays the branch in which the parts order was created.                                                                                           |
| CalculatedPrice         | This field displays the price of the given detail item before override price is taken into consideration.                                                      |
| CreationDate            | This field displays the date on which the parts order that the given detail item is attached to was created.                                                   |
| DeliveryDate            | This field displays the date on which the given part was picked up by or delivered to the customer.                                                            |
| Department              | This field displays the department in which the parts order was created.                                                                                       |
| DetailPartMessage       | This field displays the message associated with the given part detail item.                                                                                    |
| Division                | This field displays the division in which the parts order was created.                                                                                         |
| ExtendedAverageCost     | This field displays the extended average cost (average cost \* quantity) of the given part.                                                                    |
| ExtendedPrice           | This field displays the extended price (price \* quantity) of the given part.                                                                                  |
| ExtendedReplacementCost | This field displays the extended replacement cost (replacement cost \* quantity) of the given part.                                                            |
| ExtendedSellingCost     | This field displays the extended selling cost (selling cost \* quantity) of the given part.                                                                    |
| InsidePartsSalesperson  | This field displays the inside parts salesperson that sold the given parts order detail record.                                                                |
| InvoiceDate             | This field displays the date on which the given parts order was invoiced.                                                                                      |
| InvoiceNumber           | This field displays the invoice number of the given invoiced parts order.                                                                                      |
| ItemDescription         | This field displays the description of the given parts order detail item.                                                                                      |
| PartNumber              | This field displays the part number of the given part on the parts order.                                                                                      |
| ItemType                | This field displays the item type (Part for all parts, MISC for a miscellaneous charge, or EHC for an environmental handling charge) of the given detail item. |
| LastUpdateDate          | This field displays the date on which the given parts order detail item was last updated.                                                                      |
| LastUpdateUser          | This field displays the username of the user who last updated the given parts order detail item on the parts order.                                            |
| Local                   | This field displays whether the parts order should have the local sales tax applied to it.                                                                     |
| MPOReference            | This field displays the miscellaneous purchase order referenced to the given parts order, if one exists.                                                       |
| IsNoChargeTransaction   | This field displays whether the given part was sold at no charge to the customer on the given invoice.                                                         |
| OEMPrice                | This field displays the customer's selling price of the part that was received from the OEM in a price verification.                                           |
| OEMRebateAmount         | This field displays the rebate amount received from the OEM in a price verification that the cost of the transaction can be reduced by.                        |
| OrderStatus             | This field displays the status of the parts order that the given detail item is attached to.                                                                   |
| OutsidePartsSalesperson | This field displays the outside parts salesperson associated with the customer on the given parts order.                                                       |
| OverridePrice           | This field displays the override price entered for the given detail item when it was added to the parts order.                                                 |
| PartType                | This field displays the type (Part, Core, or Exchange) of the given part.                                                                                      |
| IsPartialFill           | This field displays whether the given parts order was partially filled.                                                                                        |
| PartsAccounting         | This field displays the parts accounting code associated with the given parts order invoice.                                                                   |
| PartsActionType         | This field displays the action type (sale, sale - force fill, sale - no usage update) chosen when the part was added to the parts order.                       |
| PartsOrderNumber        | This field displays the parts order number that the given detail item is attached to.                                                                          |
| PickupDeliveryMethod    | This field displays either the delivery method by which the part will be delivered to the customer or that the customer will pick it up.                       |
| IsPOSAssembly           | This field will identify if the give record is a point of sale assembly.                                                                                       |
| Price                   | This field displays the price at which the given detail item was sold (Override Price if there is one, Calculated Price if not).                               |
| PriceOverrideReason     | This field displays the price override reason associated with the given part.                                                                                  |
| Quantity                | This field displays the quantity of the given part requested on the parts order.                                                                               |
| ReadyForPickup          | This field displays whether the given detail item(s) on a parts order is(are) ready to be picked up.                                                           |
| ReplacementCost         | This field displays the replacement cost of the given part.                                                                                                    |
| ReturnReason            | This field displays the reason supplied as to why the given part was returned by the customer.                                                                 |
| SellingCost             | This field displays the cost of the given part sold on the parts order, based on either average cost or replacement cost, depending on the enterprise setting. |
| Supplier                | This field displays the supplier of the given part detail record.                                                                                              |
| UnitOfMeasure           | This field displays the units in which the given part is sold.                                                                                                 |

---
---
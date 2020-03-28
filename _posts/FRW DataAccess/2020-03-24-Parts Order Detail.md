---
layout: post
title: "Parts Order Detail"
category: "Parts" 
icon: "icon-gear"
type: "data_access" 
comments: false
description: Access to all of the detail records on open, invoiced, and/or voided parts orders.
---

---
---

### Parts Order Detail
---

This data object is used to display all of the detail records on open, invoiced, and/or voided parts orders.

This information is located in the Parts Order application in the Fusion business system.

#### URL

```
/frw/PartsOrderDetail
```
 
 <hr>
Field Details...

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
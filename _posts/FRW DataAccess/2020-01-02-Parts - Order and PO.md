---
layout: post
title: "Parts Purchase Order"
category: "Parts" 
icon: "icon-gear"
type: "data_access" comments: falsedescription: Access to Parts Order and Purchase Order within Fusion
---

---
---
### Parts Order
---

This data object is used to display all parts order header records.

This information is located within the Parts Order program in the Fusion
business system.

 <!-- SQL VIEW:  **vwIN_SSR_PartsOrder**



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

 <!-- SQL VIEW:  **vwIN_SSR_PartsOrderDetail**



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
### Parts Purchase Order
---

This data object is used to display the header information and overall totals for all of the parts purchase orders in Fusion.

This information can be found in the Parts Purchase Order program within the
Fusion business system.

 <!-- SQL VIEW:  **vwIN_SSR_PartsPO**



 -->  <hr>Field Details...

| **SQL Field Name**    | **Column Description**                                                                                                                              |
|---|---|
| AddDate               | This field displays the date on which the given purchase order was added to the system.                                                             |
| AddUser               | This field displays the username of the user who added the given purchase order to the system.                                                      |
| APVendor              | This field displays the A/P vendor associated with the given purchase order.                                                                        |
| BOPriority            | This field displays the backorder priority flag associated with the parts on the given purchase order.                                              |
| Branch                | This field displays the branch associated with the given purchase order.                                                                            |
| CoreChargeTotal       | This field displays the total price of all of the cores on the given purchase order.                                                                |
| CoreReturnTotal       | This field displays the total price of all of the returned cores on the given purchase order.                                                       |
| DirectShip            | This field displays whether the given purchase order will be filled by parts being directly shipped to a given location.                            |
| FillingBranch         | This field displays the filling branch for the given purchase order.                                                                                |
| InterBranchStockOrder | This field displays whether the given purchase order is indicated to be an interbranch stock order.                                                 |
| LastUpdateDate        | This field displays the date on which the given purchase order was last updated in the system.                                                      |
| LastUpdateUser        | This field displays the username of the user who last updated the given purchase order in the system.                                               |
| OEMReferenceNumber    | This field displays the reference number for the given purchase order assigned by the OEM interface.                                                |
| OrderedByUser         | This field displays the username of the user who ordered the given purchase order.                                                                  |
| PartsTotal            | This field displays the total price of all of the parts on the given purchase order.                                                                |
| PONumber              | This field displays the order number of the given purchase order.                                                                                   |
| PurchaseOrderDate     | This field displays the date on which the given purchase order was created (this field can be manually updated, so could differ from the add date). |
| PurchaseOrderSource   | This field displays the source of the given purchase order assigned by the OEM interface.                                                           |
| ReturnPurchaseOrder   | This field displays whether the given purchase order is indicated to be a return purchase order.                                                    |
| ShipToAddress1        | This field displays the first line of the ship to address of the given purchase order.                                                              |
| ShipToAddress2        | This field displays the second line of the ship to address of the given purchase order.                                                             |
| ShipToCity            | This field displays the city of the ship to address of the given purchase order.                                                                    |
| CompanyName           | This field displays the company name of the ship to location for the given purchase order.                                                          |
| ShipToPostalCode      | This field displays the postal code of the ship to address of the given purchase order.                                                             |
| ShipToRegion          | This field displays the region of the ship to address of the given purchase order.                                                                  |
| Status                | This field displays the status of the given purchase order.                                                                                         |
| SupplierCode          | This field displays the supplier listed on the header of the given purchase order.                                                                  |
| Name                  | This field displays the name of the supplier listed on the header of the given purchase order.                                                      |
| Total                 | This field displays the total price of the given purchase order.                                                                                    |
| TotalPieces           | This field displays the total count of all of the items on the given purchase order.                                                                |
| TotalWeight           | This field displays the total weight of all of the items on the given purchase order.                                                               |
| VendorCompanyName     | This field displays the company name of the A/P vendor associated with the given purchase order.                                                    |

---
---
### Parts Purchase Order Detail
---

This data object is used to display all parts purchase order detail records.

This information is located within the Parts Purchase Order program within the
Fusion business system.

 <!-- SQL VIEW:  **vwIN_SSR_PartsPODetail**



 -->  <hr>Field Details...

| **SQL Field Name**              | **Column Description**                                                                             |
|---|---|
| AddDate                         | This field displays the date on which the given part number was added to the given purchase order. |
| AddUser                         | This field displays the user name that added the record.                                           |
| AverageCost                     | This field displays the average cost of the part.                                                  |
| BinLocation                     | This field displays the parts bin location.                                                        |
| Branch                          | This field displays the branch the purchase order was created in.                                  |
| CoreCost                        | This field displays the replacement cost of a core part.                                           |
| CoreImportCost                  | This field displays the import cost for the given core part.                                       |
| CorePartDescription             | This field displays the description of the core part number attached to the part.                  |
| CorePartNumber                  | This field displays the number attached to a core part.                                            |
| Cost                            | This field displays the replacement cost of the part.                                              |
| DetailDeliveryDate              | This field displays the estimated delivery date for the given detail item.                         |
| Division                        | This field displays the company division associated with the given purchase order.                 |
| ExtendedAverageCost             | This field displays the extended average cost of the part.                                         |
| ExtendedCoreCost                | This field displays the extended replacement cost of a core part.                                  |
| ExtendedCost                    | This field displays the extended replacement cost of the part.                                     |
| ExtendedInherentAverageCoreCost | This field displays the extended inherent average cost of the core.                                |
| FillingBranch                   | For inter branch purchase orders, this field displays the branch filling the order.                |
| ImportCost                      | This field displays the import cost for the given part.                                            |
| InherentAverageCoreCost         | This field displays the inherent average cost of the core.                                         |
| InterBranchBackorder            | This field contains the number of the quantity ordered that will be backordered.                   |
| InterBranchStockOrder           | This field displays whether or not the given purchase order is an Inter-Branch purchase order.     |
| LastUpdateDate                  | This field displays the date on which the given purchase order detail item was last updated.       |
| UpdateUser                      | This field displays the user name of the individual who made the update.                           |
| Message                         | This field displays the user entered message/comment for the given purchase order detail item.     |
| PartDescription                 | This field displays the description of the given part number.                                      |
| PartNumber                      | This field displays the given purchase order detail items part number.                             |
| PONumber                        | This field displays the purchase order number assigned to the given detail item.                   |
| Quantity                        | This field displays the quantity requested for a given item.                                       |
| Status                          | This field displays the status of the given purchase order.                                        |
| StockStatus                     | This field displays the part's stock status (stock, non-stock, obsolete, superseded, etc.).        |
| SupplierCode                    | This field displays the code attached to a supplier for a part.                                    |
| SupplierName                    | This field displays the name of the supplier the purchase order if for.                            |
| UnitOfMeasure                   | This field displays the unit of measure for the given purchase order detail item.                  |
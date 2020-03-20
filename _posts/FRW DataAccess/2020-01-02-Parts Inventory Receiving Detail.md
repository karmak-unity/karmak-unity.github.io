---
layout: post
title: "Parts Inventory Receiving Detail"
category: "Parts"
icon: "icon-gear"
type: "data_access" comments: falsedescription: Provides detailed information related to parts received against a purchase order.
---

---
---

This data object is used to provides detailed information related to parts received against a purchase order.

<hr>### Field Details...

| Field                            |  Definition                                                                                                             |
|----------------------------------|---------------------------------------------------------------------------------------------------------------|
| BranchID                         | ID of the branch associated with the receiving record                                                         |
| ReceiveInventoryDetailID         | ID assigned to the individual receiving records.                                                              |
| ReceiveInventoryHeaderID         | ID assigned to the receiving record.                                                                          |
| PartsInventoryDetailID           | ID assigned to a part record for a specific branch.                                                           |
| ExchangeReceiveInventoryDetailID | ID assigned to the Inh part record for a specific branch.                                                     |
| PartPurchaseOrderHeaderID        | ID assigned to the Purchase Order header                                                                      |
| PartPurchaseOrderDetailID        | ID assigned to each part record on a Purchase Order.                                                          |
| ItemType                         | Designates what type of item the specific line is, Part, Exc, Ret or Misc                                     |
| SupplierID                       | ID assigned to the Supplier of item received                                                                  |
| Supplier                         | Supplier of item received                                                                                     |
| Item                             | Item received (part or misc charge)                                                                           |
| ItemDescription                  | Description of the item received                                                                              |
| Quantity                         | Quantity received                                                                                             |
| Cost                             | Cost of the item received                                                                                     |
| OverrideCost                     | Override cost of the item received                                                                            |
| ExtendedCost                     | Extended cost of the item received (cost x quantity)                                                          |
| CoreSupplier                     | Supplier of the inherent core associated with the exchange part received                                      |
| CorePartNumber                   | Inherent core part number associated with the exchange part received                                          |
| CorePartDescription              | Description of the inherent core associated with the exchange part received                                   |
| CoreCost                         | Cost of the inherent core assoicated with the exchange part received                                          |
| CoreExtendedCost                 | Extended cost of the inherent core associated with the exchange part received (core cost x quantity received) |
| SupplierBackOrderQuantity        | This number denotes the quantity that is still due from the supplier.                                         |
| QuantityOrdered                  | Quantity ordered on the original purchase order                                                               |
| QuantityRemaining                | Remaining quantity not yet received (quantity ordered - quantity received)                                    |
| BinLocation                      | Bin location for the part received                                                                            |
| PostingReference                 | Posting reference number assigned when the purchase order was received                                        |
| PackingSlip                      | Packing slip number associated with the purchase order received                                               |
| IsManuallyReferenced             | Denotes if the Posting Reference has been Manually Referenced.                                                |
| IsPosted                         | Denotes if item is posted                                                                                     |
| AddDate                          | Date the record was added to the system                                                                       |
| AddUser                          | User that added the record to the system                                                                      |
| LastUpdateDate                   | Date the record was last updated                                                                              |
| ReceivedDate                     | Date item was received                                                                                        |
| LastUpdateUser                   | User that last updated the record                                                                             |
| InterbranchShipmentNumber        | This number denotes the shipment record from the Interbranch order                                            |
| PurchaseOrderNumber              | Purchase order number received against                                                                        |
| PurchaseOrderDate                | Date the purchase order was finalized                                                                         |
| Branch                           | Branch in which the associated purchase order was created                                                     |
| FromBranch                       | For Interbranch orders, this is the branch that transferred the parts.                                        |
| ExcludeFromCurrencyExchange      | Determines if the Import Cost is used.                                                                        |
| CoreExcludeFromCurrencyExchange  | Determines if the the Core Import Cost is used.                                                               |
| ImportCost                       | Foreign import cost of the part received                                                                      |
| CoreImportCost                   | Foreign import cost of the inherent core associated with the exchange part received                           |
| OverrideCurrencyExchangeRate     | Override currency exchange rate of the item received                                                          |

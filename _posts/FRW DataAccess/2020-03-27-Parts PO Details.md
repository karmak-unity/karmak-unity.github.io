---
layout: post
title: "Parts Purchase Order Detail"
category: "Parts" 
icon: "icon-gear"
type: "data_access" 
comments: false
description: Access to Purchase Order Detail within Fusion
---

---
---

#### URL
```
/frw/PartsPODetail
```
---

This data object is used to display all parts purchase order detail records.

This information is located within the Parts Purchase Order program within the Fusion business system.


<hr>
Field Details...

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
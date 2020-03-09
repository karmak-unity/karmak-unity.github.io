---
layout: post
title: "Parts Purchase Order"
category: "Parts" 
icon: "icon-gear"
type: "data_access" comments: falsedescription: Access to Purchase Order within Fusion
---

---
---

This data object is used to display the header information and overall totals for all of the parts purchase orders in Fusion.

This information can be found in the Parts Purchase Order program within the
Fusion business system.

 <!-- 


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

 <!-- 


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
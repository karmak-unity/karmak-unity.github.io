---
layout: post
title: "Parts Kit Assembly Detail"
category: "Parts" 
icon: "icon-gear"
type: "data_access" comments: falsedescription: Access to various Parts related endpoints
---

---
---


This data object is used to show a listing of all kits and assemblies and their detail records.

This information is located in the Parts Inventory program within the Fusion
business system.

 #### URL 
```
/frw/KitAssemblyDetail
```  <hr>Field Details...

| **SQL Field Name**                   | **Column Description**                                                                                                                       |
|---|---|
| AverageCost                          | This field displays the average cost of a given kit/assembly part.                                                                           |
| BinLocation                          | This field displays the location of a kit/assembly part.                                                                                     |
| Branch                               | This field displays the branch associated with the kit/assembly part number.                                                                 |
| DetailAverageCost                    | This field displays the average cost of a detail part. When the detail type is core then this field displays the inherent average core cost. |
| DetailBinLocation                    | This field displays the location of a detail part.                                                                                           |
| DetailPartDescription                | This field displays the description of a detail part or miscellaneous charge.                                                                |
| DetailPartNumber                     | This field displays the number attached to a detail part.                                                                                    |
| DetailQuantityAvailable              | This field displays the quantity available of a detail part.                                                                                 |
| DetailQuantityRequired               | This field displays the quantity required in a kit or assembly of a detail part or miscellaneous charge.                                     |
| DetailReplacementCost                | This field displays the replacement cost of a detail part.                                                                                   |
| DetailStockStatus                    | This field displays the detail part's stock status (stock, non-stock, obsolete, superseded, etc.).                                           |
| DetailSupplier                       | This field displays the supplier of a given detail part.                                                                                     |
| DetailType                           | This field displays the type of detail record (core, exchange, miscellaneous charge, part, etc.).                                            |
| KitAndAssemblyType                   | This field displays whether a part is a part, kit, or assembly.                                                                              |
| PartDescription                      | This field displays the description of the kit/assembly part.                                                                                |
| PartNumber                           | This field displays the part number of the kit/assembly part.                                                                                |
| PrintDetailOnInvoice                 | This field displays whether or not the detail of a kit or assembly should print on a customer's invoice.                                     |
| PrintRelatedCoreDetailOnInvoice      | This field displays whether or not any core charges in the detail of a kit or assembly should print on a customer's invoice.                 |
| QuantityAvailable                    | This field displays the quantity available of a certain part.                                                                                |
| ReplacementCost                      | This field displays the replacement cost of a given part.                                                                                    |
| StockStatus                          | This field displays the kit/assembly part's stock status (stock, non-stock, obsolete, superseded, etc.).                                     |
| Supplier                             | This field displays the supplier of the kit/assembly part.                                                                                   |
| SupplierName                         | This field displays the name of a supplier for a part for a kit or assembly.                                                                 |
| UpdateDetailSalesHistoryAsKitIsBuilt | This field displays whether or not the detail sales history should be updated as a kit is built.                                             |

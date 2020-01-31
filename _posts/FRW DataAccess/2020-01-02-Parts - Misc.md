---
layout: post
title: "Parts Misc"
category: "Parts" 
icon: "icon-gear"
type: "data_access" comments: falsedescription: Access to various Parts related endpoints
---

---
---
### Parts Kit Assembly Detail
---

This data object is used to show a listing of all kits and assemblies and their detail records.

This information is located in the Parts Inventory program within the Fusion
business system.

 <!-- 


 -->  <hr>Field Details...

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

---
---
### Parts Lost Sales
---

This data object is used to show all parts lost sale records in the Fusion
business system.

This information can be found within the Parts Lost Sales program within the
Fusion business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name** | **Column Description**                                                                      |
|---|---|
| AddDate            | This field displays the date and time the given record was added to the system.             |
| User               | This field displays the user name of the user who posted a transaction.                     |
| Application        | This field displays the source application from which the lost sale originated.             |
| Branch             | This field displays the branch associated with the lost sale record.                        |
| IsCurrentYear      | This field displays the if the lost sale occurred in the current year.                      |
| CustomerNumber     | This field displays the identifying number attached to a customer.                          |
| CustomerName       | This field displays the A/R customer's name from the customer record.                       |
| LastUpdateDate     | This field displays the date and time the given record was updated.                         |
| LastUpdateUser     | This field displays the username of the last person to update the given record.             |
| LostSaleComment    | This field displays the comment related to a lost sale at the time it was recorded.         |
| LostSaleDate       | This field displays the date on which a lost sale was recorded.                             |
| LostSaleMonth      | This field displays the month of the lost sale was recorded.                                |
| LostSaleReason     | This field displays the reason selected for a lost sale.                                    |
| LostSaleYear       | This field displays the year of the lost sale was recorded.                                 |
| Description        | This field displays the description of a given part number.                                 |
| PartNumber         | This field displays the part number of a part on a miscellaneous purchase order.            |
| Quantity           | This field displays the quantity requested for a given item.                                |
| ReplacementCost    | This field displays the replacement cost of a given part.                                   |
| StockStatus        | This field displays the part's stock status (stock, non-stock, obsolete, superseded, etc.). |
| Supplier           | This field displays the supplier of an item on a miscellaneous purchase order.              |

---
---
### Parts Customer Backorders
---

This data object is used to show all parts that are backordered on a parts order
or repair order.

This information can be found in the Parts Order and Repair Order programs
within the Fusion business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**  | **Column Description**                                                                                                |
|---|---|
| AddDate             | This field displays the date on which the back order was created.                                                     |
| AddUser             | This field displays the user name that added the record.                                                              |
| Street1             | This field displays line one of the street address for the customer.                                                  |
| Street2             | This field displays line two of the street address for the customer.                                                  |
| APVendor            | This field displays the A/P vendor.                                                                                   |
| APVendorName        | This field displays the name of an  Accounts Payable vendor associated with a customer core right to return.          |
| BackorderAging      | This field displays the aging category the part falls into based on the Add Date of the part to the order.            |
| BackorderDate       | This field displays the date on which a part was backordered.                                                         |
| BackorderPriority   | This field displays the backorder priority flag assigned to the parts.                                                |
| Quantity            | This field displays the quantity requested for a given item.                                                          |
| Status              | This field displays the status of a given backorder.                                                                  |
| BranchCode          | This field displays the branch that requested the order.                                                              |
| City                | This field displays Bill-To city of the customer the back order is associated with.                                   |
| CoreDescription     | This field displays the description of a core associated with a part.                                                 |
| CorePartNumber      | This field displays the number attached to a core part.                                                               |
| CorePrice           | This field displays the price of the inherent core.                                                                   |
| CoreSupplierCode    | This field displays the code attached to a supplier for a core part.                                                  |
| CustomerKey         | This field displays the customer identification number.                                                               |
| CompanyName         | This field displays the company name of the customer associated with the back order.                                  |
| DaysOld             | This field displays the age of a given back ordered part, expressed in number of days.                                |
| Department          | This field displays the department that requested the part.                                                           |
| Description         | This field displays the description of a given part.                                                                  |
| DetailDeliveryDate  | This field displays the expected delivery date of the given back ordered part.                                        |
| FromBranch          | This field displays the filling branch of the given back ordered part.                                                |
| InsideSalesperson   | This field displays the inside salesperson attached to a backorder.                                                   |
| DirectShip          | This field displays whether or not an item will be a direct ship to a given location.                                 |
| LastUpdate          | This field displays the date on which the backorder was last updated.                                                 |
| UpdateUser          | This field displays the user name of the individual who made the update.                                              |
| OrderingDepartment  | This field displays the module, parts or service, that ordered the part.                                              |
| NoCharge            | This field displays whether or not the part was sold as no charge to the customer on a parts or repair order invoice. |
| OriginalCorePrice   | This field displays the original price of the part.                                                                   |
| OriginalPrice       | This field displays the original price of the inherent core.                                                          |
| Salesperson         | This field displays the salesperson attached to a customer.                                                           |
| PartNumber          | This field displays the part number of the part being backordered.                                                    |
| PartTypeDescription | This field displays the description of a part type for a backordered part.                                            |
| ShipComplete        | This field displays whether or not the given backorderd part can be partially filled or not.                          |
| SalesOrderNumber    | This field displays the number attached to a sales order.                                                             |
| PostalCode          | This field displays the customer's postal code.                                                                       |
| Price               | This field displays the price the customer was charged for the part.                                                  |
| PONumber            | This field displays the Parts Purchase Order Number.                                                                  |
| PurchaseOrderStatus | This field displays the order status of the backorder.                                                                |
| QuantityAvailable   | 0                                                                                                                     |
| Region              | This field displays the customer's region or state.                                                                   |
| RepairOrderNumber   | This field displays the number attached to a repair order.                                                            |
| CustomerPONumber    | This field displays the Customer's purchase order number.                                                             |
| SupplierCode        | This field displays the code attached to a supplier for a part.                                                       |
| TaskNumber          | This field displays the number attached to a given task.                                                              |

---
---
### Parts Committed
---

This data object is used to display all parts that have been committed on parts
order, repair orders, and inter-branch orders.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**      | **Column Description**                                                                                                                                                                                                                                                      |
|---|---|
| IsAssemblyDetail        | This field displays whether or not the given committed part is part of an assembly.                                                                                                                                                                                         |
| AssemblyPartNumber      | This field displays the assembly part number the given part is associated with.                                                                                                                                                                                             |
| AverageCost             | This field displays the average cost of the part at the time it was committed to the order.                                                                                                                                                                                 |
| Branch                  | This field displays the branch the part is committed in.                                                                                                                                                                                                                    |
| CommittedDate           | This field displays the date on which parts were committed.                                                                                                                                                                                                                 |
| CustomerNumber          | This field displays the identifying number attached to a customer.                                                                                                                                                                                                          |
| CompanyName             | This field displays the company name of the customer associated with the order.                                                                                                                                                                                             |
| ExtendedAverageCost     | This field displays the extended average cost of the part at the time it was committed to the order.                                                                                                                                                                        |
| ExtendedReplacementCost | This field displays the extended replacement cost of the part at the time it was committed to the order.                                                                                                                                                                    |
| ExtendedSellingPrice    | This field displays the extended selling price of the given part on the given order.                                                                                                                                                                                        |
| Module                  | This field displays the module the comitted part originated from.  Orders with a module of "Service" originate from Repair Orders.  Orders with a module of "Parts" originate from Parts Orders. Orders with a module of "P/O" originate from inter-branch purchase orders. |
| OrderNumber             | This field displays the order number the part is committed on.                                                                                                                                                                                                              |
| Description             | This field displays the description of a given part.                                                                                                                                                                                                                        |
| PartNumber              | This field displays the part number of the committed part.                                                                                                                                                                                                                  |
| PartType                | This field displays the part type (Part, EXC, INH, or RET) of the given part.                                                                                                                                                                                               |
| Quantity                | This field displays the quantity requested for a given item.                                                                                                                                                                                                                |
| SellingCost             | This field displays the replacement cost of the given part at the time the part was committed to the order.                                                                                                                                                                 |
| RequestingBranch        | This field displays the branch that has requested the part.                                                                                                                                                                                                                 |
| SellingPrice            | This field displays the selling price of a given part.                                                                                                                                                                                                                      |
| SupplierCode            | This field displays the supplier associated with the committed part.                                                                                                                                                                                                        |

---
---
### Parts Messages
---

This data object is used to show a list of all parts messages set up.

This information can be located within the Parts Messages program within the
Fusion business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name** | **Column Description**                                                       |
|---|---|
| AddDate            | This field displays the date on which the part message was added.            |
| AddUser            | This field displays the user name that added the record.                     |
| Branch             | This field displays the branch associated with the part message.             |
| LastUpdate         | This field displays the date on which the given message was last updated.    |
| UpdateUser         | This field displays the user name of the individual who made the update.     |
| MessageDescription | This field displays the description of a parts message.                      |
| MessageType        | This field displays the type of parts message.                               |
| PartDescription    | This field displays the description of the part associated with the message. |
| PartNumber         | This field displays the part number of the part associated with the message. |
| PartType           | This field displays the type of a part.                                      |
| SupplierCode       | This field displays the code attached to a supplier for a part.              |


---
---
### Parts Transactions
---

This data object is used to display all parts transaction records from the
Fusion business system.  Transactions where the price level fields were updated
due to pricing changes will have the field column set to be "blank", and you can
see the changes by referencing the price level and previous price level fields.

This information can be found in the Parts Transactions program within the
Fusion business system. 

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**              | **Column Description**                                                                                                                                                                                                                                                                                                                 |
|---|---|
| Application                     | This field displays the application in which the part transaction originated.                                                                                                                                                                                                                                                          |
| AverageCost                     | This field displays the parts new average cost after the transaction occurred.                                                                                                                                                                                                                                                         |
| PartBranch                      | This field displays the branch associated with the part transaction.                                                                                                                                                                                                                                                                   |
| DateTime                        | This field displays the date on which the part transaction took place.                                                                                                                                                                                                                                                                 |
| PartDescription                 | This field displays the description of the part the transactions is for.                                                                                                                                                                                                                                                               |
| Difference                      | This field displays the difference between the new and old value (New Value - Old Value).                                                                                                                                                                                                                                              |
| ChangedField                    | This field displays the name of the parts inventory field that was changed as a part of the part transaction.  Transactions where the price level fields were updated due to pricing changes will have the field column set to be "blank", and you can see the changes by referencing the price level and previous price level fields. |
| InherentAverageCost             | This field displays the Inherent Average Cost of core records.                                                                                                                                                                                                                                                                         |
| InherentReplacementCost         | This field displays the Inherent Replacement Cost of core records.                                                                                                                                                                                                                                                                     |
| ListPrice                       | This field displays the given part's new list price at the time the transaction took place based on the parts cost change.  This value would be different from Previous List Price on transactions where replacement cost was changed and price were recalculated.                                                                     |
| NewValue                        | This field displays the New Value based on the Changed field.                                                                                                                                                                                                                                                                          |
| OldValue                        | This field displays the Old Value based on the Changed field.                                                                                                                                                                                                                                                                          |
| PartNumber                      | This field displays the part number of the part transaction is for.                                                                                                                                                                                                                                                                    |
| PartType                        | This field displays the type of a part.                                                                                                                                                                                                                                                                                                |
| PreviousAverageCost             | This field displays the average cost of the given part prior to the transaction taking place.                                                                                                                                                                                                                                          |
| PreviousInherentAverageCost     | This field displays the average cost of the inherent core associated with the given part prior to the transaction taking place.                                                                                                                                                                                                        |
| PreviousInherentReplacementCost | This field displays the replacement cost of the inherent core associated with the given part prior to the transaction taking place.                                                                                                                                                                                                    |
| PreviousListPrice               | This field displays the given part's list price prior to the transaction taking place.                                                                                                                                                                                                                                                 |
| PreviousPrice1                  | This field displays the given part's price level 1 prior to the transaction taking place.                                                                                                                                                                                                                                              |
| PreviousPrice2                  | This field displays the given part's price level 2 prior to the transaction taking place.                                                                                                                                                                                                                                              |
| PreviousPrice3                  | This field displays the given part's price level 3 prior to the transaction taking place.                                                                                                                                                                                                                                              |
| PreviousPrice4                  | This field displays the given part's price level 4 prior to the transaction taking place.                                                                                                                                                                                                                                              |
| PreviousPrice5                  | This field displays the given part's price level 5 prior to the transaction taking place.                                                                                                                                                                                                                                              |
| PreviousPrice6                  | This field displays the given part's price level 6 prior to the transaction taking place.                                                                                                                                                                                                                                              |
| PreviousPrice7                  | This field displays the given part's price level 7 prior to the transaction taking place.                                                                                                                                                                                                                                              |
| PreviousQuantityAvailable       | This field displays the quantity available of the given part prior to the transaction taking place.                                                                                                                                                                                                                                    |
| PreviousReplacementCost         | This field displays the replacement cost of the given part prior to the transaction taking place.                                                                                                                                                                                                                                      |
| Price1                          | This field displays the given part's new price level 1 at the time the transaction took place.  This value would be different from Previous Price 1 on transactions where replacement cost was changed and price were recalculated.                                                                                                    |
| Price2                          | This field displays the given part's new price level 2 at the time the transaction took place.  This value would be different from Previous Price 2 on transactions where replacement cost was changed and price were recalculated.                                                                                                    |
| Price3                          | This field displays the given part's new price level 3 at the time the transaction took place.  This value would be different from Previous Price 3 on transactions where replacement cost was changed and price were recalculated.                                                                                                    |
| Price4                          | This field displays the given part's new price level 4 at the time the transaction took place.  This value would be different from Previous Price 4 on transactions where replacement cost was changed and price were recalculated.                                                                                                    |
| Price5                          | This field displays the given part's new price level 5 at the time the transaction took place.  This value would be different from Previous Price 5 on transactions where replacement cost was changed and price were recalculated.                                                                                                    |
| Price6                          | This field displays the given part's new price level 6 at the time the transaction took place.  This value would be different from Previous Price 6 on transactions where replacement cost was changed and price were recalculated.                                                                                                    |
| Price7                          | This field displays the given part's new price level 7 at the time the transaction took place.  This value would be different from Previous Price 7 on transactions where replacement cost was changed and price were recalculated.                                                                                                    |
| QuantityAdjustmentReason        | This field displays the description of reasoning behind a quantity adjustment.                                                                                                                                                                                                                                                         |
| QuantityAvailable               | This field displays the quantity available of the part at the time the transaction took place.                                                                                                                                                                                                                                         |
| ReplacementCost                 | This field displays the parts new replacement cost after the transaction occurred.                                                                                                                                                                                                                                                     |
| SourceDocument                  | This field displays the Invoice Number or Price File record that initiated the change.                                                                                                                                                                                                                                                 |
| Supplier                        | This field displays the supplier associated with the given part transaction.                                                                                                                                                                                                                                                           |
| SupplierName                    | This field displays the supplier's name.                                                                                                                                                                                                                                                                                               |
| ChangeAction                    | This field displays the type of parts transaction that was completed (add, update, delete, merge).                                                                                                                                                                                                                                     |
| Username                        | This field displays the user responsible for the parts transaction.                                                                                                                                                                                                                                                                    |

---
---
### Parts Vendor Rebates
---

This data object is used to display all vendor rebate information.

This information can be found in the Vendor Rebate program within the Fusion
business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**                     | **Column Description**                                                                                                                                                                                           |
|---|---|
| AddUser                                | This field displays the user name that added the record.                                                                                                                                                         |
| AverageCost                            | This field displays the average cost of a given part.                                                                                                                                                            |
| Branch                                 | This field displays the branch associated with the rebate.                                                                                                                                                       |
| CalculateCommissionsBasedOnRebatedCost | This field indicates salesman commission will be calculated based on the rebated cost of the transaction. This field will always be set with the same setting as the Use Rebated Cost at Time of Sale check box. |
| Code1                                  | This field displays the Code 1 field of a part record.                                                                                                                                                           |
| Code2                                  | This field displays the Code 2 field of a part record.                                                                                                                                                           |
| Code3                                  | This field displays the Code 3 field of a part record.                                                                                                                                                           |
| Code4                                  | This field displays the Code 4 field of a part record.                                                                                                                                                           |
| Code5                                  | This field displays the Code 5 field of a part record.                                                                                                                                                           |
| Customer                               | This field displays the customer attached to the given vendor rebate.                                                                                                                                            |
| CustomerName                           | This field displays the customer's name from the customer record.                                                                                                                                                |
| CustomerPricingType                    | This field indicates the customer pricing type for the rebate record.                                                                                                                                            |
| ExpirationDate                         | This field displays the date on which the given rebate expires.                                                                                                                                                  |
| ExtendedRebateAmount                   | This field contains the extended rebate amount (Quantity \* Rebate Amount).                                                                                                                                      |
| InsideSalesperson                      | This field displays the inside salesperson attached to the rebate.                                                                                                                                               |
| InvoiceDate                            | This field displays the invoice date of the parts order associated with the rebate record.                                                                                                                       |
| InvoiceNumber                          | This field displays the invoice number of the parts order associated with the given rebate record.                                                                                                               |
| LastUpdate                             | This field displays the date on which the give rebate was last updated.                                                                                                                                          |
| UpdateUser                             | This field displays the user name of the individual who made the update.                                                                                                                                         |
| Multiplier                             | This field contains the multiplier used to calculate the amount of the rebate.                                                                                                                                   |
| OutsideSalesperson                     | This field displays the outside salesperson who is attached to a given rebate invoice.                                                                                                                           |
| PartDescription                        | This field displays the description of the part that is being rebated.                                                                                                                                           |
| PartNumber                             | This field displays the part number of the part being rebated.                                                                                                                                                   |
| PriceFileSource                        | This field contains the source of the price file used to calculate the rebate.                                                                                                                                   |
| PriceLevel                             | This field contains the price level used to calculate the rebate (List, Price 1-7, Replacement Cost).                                                                                                            |
| Quantity                               | This field displays the quantity sold for a given item.                                                                                                                                                          |
| RebateAmount                           | This field contains the rebate amount.                                                                                                                                                                           |
| RecordNotes                            | This field contains notes that describe the rebate.                                                                                                                                                              |
| ReplacementCost                        | This field displays the replacement cost of a given part.                                                                                                                                                        |
| SellingPrice                           | This field displays the selling price of a given part.                                                                                                                                                           |
| StockClass                             | This field displays a subset within a supplier, typically used in pricing and typically provided by the manufacturer.                                                                                            |
| Supplier                               | This field displays the supplier of the rebated part.                                                                                                                                                            |
| UseRebatedCostAtTimeOfSale             | This setting indicates whether the rebate amount was used to calculate the cost of the transaction.                                                                                                              |
| ValuePriceLevel                        | This field contains the price the rebate was calculated from if it was calculated from an inventory price.                                                                                                       |
| Vendor                                 | This field displays the vendor attached to a given rebate invoice.                                                                                                                                               |
| VendorPrice                            | This field contains the price the rebate was calculated from if it was calculated from a price file price.                                                                                                       |
| VendorPriceDescription                 | This field contains a description of the vendor price from the price file used to calculate the rebate.                                                                                                          |

---
---
### Parts Supplier
---

This data object is used to show all suppliers that are set up within the Fusion
business system.

This information can be found within the Supplier record in the Fusion business
system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**            | **Column Description**                                                                                                                                                                                                                                   |
|---|---|
| AccountingGroup               | This field displays the accounting group field of the given supplier that will populate in a new part record.                                                                                                                                            |
| AddDate                       | This field displays the date on which the given supplier was added in the Business System.                                                                                                                                                               |
| AddUser                       | This field displays the user name that added the record.                                                                                                                                                                                                 |
| Address1                      | This field displays the primary address line 1 of the supplier.                                                                                                                                                                                          |
| Address2                      | This field displays the primary address line 2 of the supplier.                                                                                                                                                                                          |
| AlternateSupplier             | This field displays the partent supplier for the given supplier.                                                                                                                                                                                         |
| APVendor                      | This field displays the A/P vendor.                                                                                                                                                                                                                      |
| CompanyName                   | This field displays the company name of an A/P vendor associated with the supplier.                                                                                                                                                                      |
| BarCodeMultiplier             | This field displays the multipler used when scanning parts in during bar code receiving of the given supplier that will populate in a new part record.                                                                                                   |
| BuyTime                       | This field displays the buy time field of the given supplier that will populate in a new part record.                                                                                                                                                    |
| CellPhone                     | This field displays the primary cell phone of the supplier.                                                                                                                                                                                              |
| City                          | This field displays the primary city of the supplier.                                                                                                                                                                                                    |
| Code1                         | This field displays the Code 1 field of the given supplier that will populate in a new part record.                                                                                                                                                      |
| Code2                         | This field displays the Code 2 field of the given supplier that will populate in a new part record.                                                                                                                                                      |
| Code3                         | This field displays the Code 3 field of the given supplier that will populate in a new part record.                                                                                                                                                      |
| Code4                         | This field displays the Code 4 field of the given supplier that will populate in a new part record.                                                                                                                                                      |
| Code5                         | This field displays the Code 5 field of the given supplier that will populate in a new part record.                                                                                                                                                      |
| CoreRightToReturnDaysCustomer | This field displays the number of days before the right to return to vendor expires.                                                                                                                                                                     |
| CoreRightToReturnDaysSupplier | This field displays the number of days a customer has to return a core before the right to return expires.                                                                                                                                               |
| Country                       | This field displays the primary country of the supplier.                                                                                                                                                                                                 |
| County                        | This field displays the primary county of the supplier.                                                                                                                                                                                                  |
| CurrencyCode                  | This field displays the currency code  of the given supplier that will populate in a new part record.                                                                                                                                                    |
| CurrencyExchangeBroker        | This field displays the currency exchange broker field of the given supplier that will populate in a new part record.                                                                                                                                    |
| DaysOfStock                   | This field displays the number of days of stock that should be carried in inventory.                                                                                                                                                                     |
| DutyCode                      | This field displays the duty rate of the given supplier that will populate in a new part record.                                                                                                                                                         |
| E-MailAddress                 | This field displays the primary E-mail of the supplier.                                                                                                                                                                                                  |
| Fax                           | This field displays the primary fax number of the supplier.                                                                                                                                                                                              |
| FirstName                     | This field displays the first name of the primary contact of the supplier.                                                                                                                                                                               |
| ImportFreightMultiplier       | This field displays the freight multiplier of the given supplier that will populate in a new part record.                                                                                                                                                |
| Inactive                      | This field displays whether or not a given supplier record is set to inactive.                                                                                                                                                                           |
| LastName                      | This field displays the last name of the primary contact of the supplier.                                                                                                                                                                                |
| LastOrderDate                 | This field displays the date on which a part was last ordered.                                                                                                                                                                                           |
| LastUpdateDate                | This field displays the last updated of the given supplier.                                                                                                                                                                                              |
| LastUpdateUser                | This field displays the user who last updated the given supplier.                                                                                                                                                                                        |
| LeadTime                      | This field displays the number of days between placing an order until receiving an order.                                                                                                                                                                |
| ListMultiplier                | This field displays the multipler associated with list price of the given supplier that will populate in a new part record.                                                                                                                              |
| ManufacturerCode              | This field displays the manufacturerer code of the given supplier that will populate in a new part record.                                                                                                                                               |
| MinimumOrderDollar            | This field displays the minimum order, expressed in dollars, required by a supplier.                                                                                                                                                                     |
| MaximumOrderWeight            | This field displays the maximum order weight for a supplier.                                                                                                                                                                                             |
| MinimumReturnDollar           | This field displays the minimum order, expressed in dollars, required by a supplier for return orders.                                                                                                                                                   |
| MinimumReturnWeight           | This field displays the minimum weight, required by a supplier for return orders.                                                                                                                                                                        |
| OEMBreakdown                  | This field identifies if the given supplier is purchased from an OEM.                                                                                                                                                                                    |
| IsOEMBreakdownPrinted         | This field identifies the default value for the given supplier will have additional classification on some reports that will populate in a new part record.                                                                                              |
| OfficePhone                   | This field displays the primary office phone of the supplier.                                                                                                                                                                                            |
| OrderFrequency                | This field displays how often you place an order (once a week, daily, etc.).                                                                                                                                                                             |
| OrderGroup                    | This field displays the order group attached to the supplier.                                                                                                                                                                                            |
| PostalCode                    | This field displays the primary postal code of the supplier.                                                                                                                                                                                             |
| Price1Multiplier              | This field displays the price 1 multiplier of the given supplier that will populate in a new part record.                                                                                                                                                |
| Price2Multiplier              | This field displays the price 2 multiplier of the given supplier that will populate in a new part record.                                                                                                                                                |
| Price3Multiplier              | This field displays the price 3 multiplier of the given supplier that will populate in a new part record.                                                                                                                                                |
| Price4Multiplier              | This field displays the price 4 multiplier of the given supplier that will populate in a new part record.                                                                                                                                                |
| Price5Multiplier              | This field displays the price 5 multiplier of the given supplier that will populate in a new part record.                                                                                                                                                |
| Price6Multiplier              | This field displays the price 6 multiplier of the given supplier that will populate in a new part record.                                                                                                                                                |
| Price7Multiplier              | This field displays the price 7 multiplier of the given supplier that will populate in a new part record.                                                                                                                                                |
| PriceFileSource               | This field identifies the price file associated with the given supplier that will populate in a new part record.                                                                                                                                         |
| PriceGroup                    | This field identifies the price group associated with the given supllier that will populate in a new part record. Used to group like parts together for customer special pricing.                                                                        |
| ProductClass                  | This field displays the product class  of the given supplier that will populate in a new part record.                                                                                                                                                    |
| PurchaseMethod                | This field displays the default purchase method of the given supplier that will be populated on a new part record for the supplier.                                                                                                                      |
| Region                        | This field displays the primary region of the supplier.                                                                                                                                                                                                  |
| ReplacementCostMultiplier     | This field displays the default  replacement cost multiplier of the given supplier that will be populated on a new part record for the supplier.                                                                                                         |
| SafetyStockPercent            | This field displays the default safety stock percent of the give supplier, which is a percentage between 0 and 100 that an order point will be padded. This field fill be populated with this amount when a new part record is created for the supplier. |
| Salutation                    | This field displays the salutation of the primary contact of the supplier.                                                                                                                                                                               |
| Seasonal                      | This field displays whether or not a part is seasonal (80% of sales of a given part occur in six consecutive months or less).                                                                                                                            |
| ShopPhone                     | This field displays the primary shop phone of the supplier.                                                                                                                                                                                              |
| StockClass                    | This field displays a subset within a supplier, typically used in pricing and typically provided by the manufacturer.                                                                                                                                    |
| SuggestedOrderMonths          | This field displays the number of months of sales history to consider when determining purchase orders for a supplier.                                                                                                                                   |
| SupplierCode                  | This field displays the code attached to a supplier for a part.                                                                                                                                                                                          |
| NAME                          | This field displays the name of the supplier.                                                                                                                                                                                                            |
| Title                         | This field displays the title of the primary contact of the supplier.                                                                                                                                                                                    |
| UnitOfMeasure                 | This field deipslays the default unit of measure for the given supplier and is populated on new part records.                                                                                                                                            |
| UpdateFromPriceFile           | This field displays the default value for the given supplier. This will determine whether or not a part number is updated from the price file- if unchecked, users manually control pricing on new part records.                                         |
| WebAddress                    | This field displays the primary web address of the supplier.                                                                                                                                                                                             |

---
---
### Parts Supplier Core RTR
---

This data object is used to show all supplier core right to return records.

This information is located in the Supplier Core Right to Return program in the
Fusion business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**               | **Column Description**                                                                                       |
|---|---|
| AddDateTime                      | This field displays the date on which the record was added.                                                  |
| AddUser                          | This field displays the user name that added the record.                                                     |
| APVendor                         | This field displays the A/P vendor.                                                                          |
| APVendorName                     | This field displays the name of an  Accounts Payable vendor associated with a customer core right to return. |
| BranchCode                       | This field displays the code identifying a branch associated with an Accounts Receivable invoice.            |
| Description                      | This field displays the description of a given part.                                                         |
| PartNumber                       | This field displays the core part number the customer has the right to return.                               |
| CoreRightToReturnDaysSupplier    | This field displays the number of days a customer has to return a core before the right to return expires.   |
| CoreSupplier                     | This field displays the supplier of a core part associated with an exchange part.                            |
| ExpirationDate                   | This field displays the date on which the customer's right to return expires.                                |
| LastUpdateTime                   | This field displays the last date and time the record was updated.                                           |
| UpdateUser                       | This field displays the user name of the individual who made the update.                                     |
| PostingReference                 | This field displays the posting reference number attached to an invoice.                                     |
| QuantityAvailable                | This field displays the quantity available of a certain part.                                                |
| QuantityReceived                 | This field displays the quantity of a part received.                                                         |
| QuantityRemaining                | This field displays the number of cores owed for the given supplier.                                         |
| QuantityReturned                 | This field displays the quantity of a core returned.                                                         |
| ReceivedCost                     | This field displays the cost of a part at the time of receiving.                                             |
| ReceivedDate                     | This field displays the date on which a purchase order was received.                                         |
| TotalOwedForPartNumber           | This field displays the number of cores owed for the given part number.                                      |
| TotalOwedToAPVendorForPartNumber | This field displays the number of cores owed for the given part number for a given AP Vendor.                |

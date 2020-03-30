---
layout: post
title: "Parts Inventory"
category: "Parts" 
icon: "icon-gear"
type: "data_access" comments: falsedescription:  Access to a concise view of all branch specific parts inventory records
---

---
---
### Parts Inventory
---

This data object is used to display a concise view of all branch specific parts inventory records. More fields related to these records can be viewed in the Parts Inventory Extended view.

This information comes from the Parts Inventory application in the Fusion
business system.

#### URL
```
/frw/PartsInventory
```
 <hr>Field Details...

| **SQL Field Name**      | **Column Description**                                                                                                                                                              |
|---|---|
| AddDate                 | This field displays the date on which the given parts inventory record was added.                                                                                                   |
| AddUser                 | This field displays the username of the user who added the given parts inventory record.                                                                                            |
| AverageCost             | This field displays the average cost or, if average cost is zero, the replacement cost of the given part.                                                                           |
| BarCode                 | This field displays the bar code for the given parts inventory record.                                                                                                              |
| BinLocation             | This field displays the bin location for the given parts inventory record.                                                                                                          |
| BranchCode              | This field displays the branch code of the branch that the given parts inventory record is associated with.                                                                         |
| Description             | This field displays the description of the given parts inventory record.                                                                                                            |
| Inactive                | This field displays whether the given parts inventory record is set to inactive.                                                                                                    |
| InherentCoreAverageCost | This field displays the inherent core average cost of the given part's inherent core or, if inherent core average cost is zero, displays the replacement cost of the inherent core. |
| LastUpdateDate          | This field displays the date on which the given parts inventory record was last updated.                                                                                            |
| LastUpdateUser          | This field displays the username of the user who last updated the given parts inventory record.                                                                                     |
| ListPrice               | This field displays the manufacturer's list price for the given parts inventory record.                                                                                             |
| PartNumber              | This field displays the part number of the given parts inventory record.                                                                                                            |
| PartType                | This field displays the part type of the given parts inventory record.                                                                                                              |
| Price1                  | This field displays the level 1, or highest, resale price for the given part.                                                                                                       |
| Price2                  | This field displays the level 2 resale price for the given part.                                                                                                                    |
| Price3                  | This field displays the level 3 resale price for the given part.                                                                                                                    |
| Price4                  | This field displays the level 4 resale price for the given part.                                                                                                                    |
| Price5                  | This field displays the level 5 resale price for the given part.                                                                                                                    |
| Price6                  | This field displays the level 6 resale price for the given part.                                                                                                                    |
| Price7                  | This field displays the level 7, or lowest, resale price for the given part.                                                                                                        |
| QuantityAvailable       | This field displays the quantity available for the given parts inventory record.                                                                                                    |
| QuantityCommitted       | This field displays the quantity that has been committed to open orders for the given parts inventory record.                                                                       |
| QuantityOnBackOrder     | This field displays the quantity that has been committed to open orders, but is not currently available in stock, for the given parts inventory record.                             |
| QuantityOnOrder         | This field displays the quantity that has been requested on open orders to vendors for the given parts inventory record.                                                            |
| ReplacementCost         | This field displays the replacement cost of the given part.                                                                                                                         |
| SellPackage             | This field displays the package size in which the given part is sold to customers.                                                                                                  |
| SupplierCode            | This field displays the supplier of the given parts inventory record.                                                                                                               |


---
---
### Inventory Extended
---

This data object is used to display all branch specific parts inventory records
and all relevant fields corresponding to the given parts inventory record from
Fusion.

This information comes from the Parts Inventory application in the Fusion
business system.

 #### URL 
```
/frw/PartsInventoryExtended
```  <hr>Field Details...

| **SQL Field Name**                    | **Column Description**                                                                                                                                                                                   |
|---|---|
| 13MonthManualPicks                    | This field displays the number of manually entered picks for the given part in the current month plus the preceding 12 months.                                                                           |
| 13MonthManualSales                    | This field displays the number of manually entered sales for the given part in the current month plus the preceding 12 months.                                                                           |
| 13MonthPicks                          | This field displays the number of picks for the given part in the current month plus the preceding 12 months.                                                                                            |
| 13MonthSales                          | This field displays the number of sales for the given part in the current month plus the preceding 12 months.                                                                                            |
| 13MonthTotalLostSales                 | This field displays the total of lost sales for the given part in the current month plus the preceding 12 months.                                                                                        |
| 13MonthTotalPicks                     | This field displays the total of picks (automatic and manual) for the given part in the current month plus the preceding 12 months.                                                                      |
| 13MonthTotalSales                     | This field displays the total of sales (automatic and manual) for the given part in the current month plus the preceding 12 months.                                                                      |
| AccountingGroup                       | This field displays the accounting group to which the given part belongs.                                                                                                                                |
| AddDate                               | This field displays the date on which the given parts inventory record was added to Fusion (this is a system generated field, which is displayed at the bottom of the Parts Inventory application).      |
| AddUser                               | This field displays the username of the user who added the given parts inventory record to Fusion.                                                                                                       |
| AlternateDescription                  | This field displays the alternate description, if one exists, for the given part from the inventory control tab on the part record.                                                                      |
| AlternateSupplier                     | This field displays the alternate supplier, if one exists, for the given part.                                                                                                                           |
| AverageCost                           | This field displays the average cost of the given part or, if average cost is zero, displays the replacement cost of that part.                                                                          |
| AverageLeadTime                       | This field displays the average lead time for the given part from the purchase control tab on the part record.                                                                                           |
| BarCode                               | This field displays the bar code associated with the given part.                                                                                                                                         |
| BarCodeMultiplier                     | This field displays the bar code multiplier for the given part from the purchase control tab on the part record.                                                                                         |
| BinLocation                           | This field displays the bin location where the given part is stored.                                                                                                                                     |
| BranchCode                            | This field displays the branch that the given parts inventory record is associated with.                                                                                                                 |
| CurrencyExchangeBroker                | This field displays the currency exchange broker associated with the given part.                                                                                                                         |
| BuyPackage                            | This field displays the buy package size for the given part from the purchase control tab on the part record.                                                                                            |
| BuyTime                               | This field displays the buy time of the given part from the purchase control tab on the part record.                                                                                                     |
| Code1                                 | This field displays the code 1 associated with the given part.                                                                                                                                           |
| Code2                                 | This field displays the code 2 associated with the given part.                                                                                                                                           |
| Code3                                 | This field displays the code 3 associated with the given part.                                                                                                                                           |
| Code4                                 | This field displays the code 4 associated with the given part.                                                                                                                                           |
| Code5                                 | This field displays the code 5 associated with the given part.                                                                                                                                           |
| CoreAverageCost                       | This field displays the average cost of the core associated with the given part or, if average cost of the core is zero, displays the replacement cost of the core.                                      |
| CoreDescription                       | This field displays the description of the core associated with the given part.                                                                                                                          |
| CoreListPrice                         | This field displays the list price of the core associated with the given part.                                                                                                                           |
| CorePartNumber                        | This field displays the part number of the core associated with the given part.                                                                                                                          |
| CorePrice1                            | This field displays the price 1 of the core associated with the given part.                                                                                                                              |
| CorePrice2                            | This field displays the price 2 of the core associated with the given part.                                                                                                                              |
| CorePrice3                            | This field displays the price 3 of the core associated with the given part.                                                                                                                              |
| CorePrice4                            | This field displays the price 4 of the core associated with the given part.                                                                                                                              |
| CorePrice5                            | This field displays the price 5 of the core associated with the given part.                                                                                                                              |
| CorePrice6                            | This field displays the price 6 of the core associated with the given part.                                                                                                                              |
| CorePrice7                            | This field displays the price 7 of the core associated with the given part.                                                                                                                              |
| CoreReplacementCost                   | This field displays the replacement cost of the core associated with the given part.                                                                                                                     |
| CoreSupplier                          | This field displays the supplier of the core associated with the given part.                                                                                                                             |
| CountryOfOrigin                       | This field displays the country from which the given part originates.                                                                                                                                    |
| CurrencyCode                          | This field displays the currency code associated with the given part.                                                                                                                                    |
| DateAdded                             | This field displays the date on which the given part record was added to inventory, from the purchase control tab in the part record (this date can be manually updated, so could differ from Add Date). |
| DaysOfStock                           | This field displays the number of days of stock that should be in inventory for the given part, from the purchase control tab in the part record.                                                        |
| DaysOutMTD                            | This field displays the number of days during the current month that the given part has been out of stock, from the purchase control tab in the part record.                                             |
| Description                           | This field displays the description associated with the given part.                                                                                                                                      |
| DutyCode                              | This field displays the duty code to be used if the given part is purchased in another currency.                                                                                                         |
| EHCCode                               | This field displays the name of the environmental handling charge to be charged when the given part is purchased.                                                                                        |
| ExcludeFromCostMatrix                 | This field displays whether the given part is excluded from cost matrix pricing.                                                                                                                         |
| ExcludeFromCurrencyExchange           | This field displays whether the given part is excluded from currency exchange.                                                                                                                           |
| ExcludeFromPriceRounding              | This field displays whether the given part is excluded from price rounding.                                                                                                                              |
| ExcludeFromVelocityPricing            | This field displays whether the given part is excluded from velocity pricing.                                                                                                                            |
| FreezeDate                            | This field displays the date through which the line point, order point, and order quantity calculations should be frozen.                                                                                |
| IsFleetStockingPartFreight            | This field displays whether the given part is flagged as a Freightliner fleet stocking list part.                                                                                                        |
| IsMissionCriticalPartFreightLiner     | This field displays whether the given part is a mission critical Freightliner part, as indicated on the OEM control tab in the part record.                                                              |
| IsRecommendedStockingPartFreightLiner | This field displays whether the given part is flagged as a Freightliner recommended stocking list part.                                                                                                  |
| FullBinQuantity                       | This field displays the quantity of the given part in a full bin, as indicated on the OEM control tab.                                                                                                   |
| ImportCost                            | This field displays the cost at which the given part was imported into the country.                                                                                                                      |
| ImportFreightMultiplier               | This field displays the freight multiplier to be used if the given part was purchased in another currency.                                                                                               |
| Inactive                              | This field displays whether the given part record has been set to inactive.                                                                                                                              |
| InherentCoreAverageCost               | This field displays the inherent core average cost of the core associated with the given part or, if the inherent core average cost is zero, displays the replacement cost of the core.                  |
| InventoryClass                        | This field displays the inventory class in which the given part is categorized.                                                                                                                          |
| JobQuantity                           | This field displays the minimum quantity of the given part needed to complete one service job.                                                                                                           |
| KitType                               | This field displays whether the given part has a kit type of kit, assembly, or part.                                                                                                                     |
| LastAveragingQuantity                 | This field displays the quantity of the given part that the latest average cost was based on.                                                                                                            |
| LastCountDate                         | This field displays the date on which the given part was last counted.                                                                                                                                   |
| LastLifoCost                          | This field displays the last LIFO cost of the given part.                                                                                                                                                |
| LastLifoDate                          | This field displays the date on which the last LIFO cost of the given part was recorded.                                                                                                                 |
| LastOrderedDate                       | This field displays the date on which the given part was last ordered.                                                                                                                                   |
| LastOutOfStockDateGMT                 | This field displays the date on which the given part was last out of stock.                                                                                                                              |
| LastPriceChangeDate                   | This field displays the date on which the price of the given part was last changed.                                                                                                                      |
| LastPriceFileUpdate                   | This field displays the date on which the price file for the given part was last updated.                                                                                                                |
| LastPuchaseCost                       | This field displays the purchase cost of the given part the last time it was purchased.                                                                                                                  |
| LastReceivedDate                      | This field displays the date on which the given part was last received into inventory.                                                                                                                   |
| LastReplacementCostChangeDate         | This field displays the date on which the replacement cost of the given part was last changed.                                                                                                           |
| LastSoldDate                          | This field displays the date on which the given part was last sold (present on a parts order or a repair order at the time of invoicing).                                                                |
| LastUpdateDate                        | This field displays the date on which the given parts inventory record was last updated in Fusion.                                                                                                       |
| LastUpdateUser                        | This field displays the username of the user who last updated the given parts inventory record in Fusion.                                                                                                |
| LeadTime                              | This field displays the number of days that will pass between placing an order and receiving an order for the given part.                                                                                |
| LifoCost                              | This field displays the current LIFO cost of the given part.                                                                                                                                             |
| LifoDate                              | This field displays the date on which the current LIFO cost of the given part was recorded.                                                                                                              |
| ListPrice                             | This field displays the list price of the given part, either from the manufacturer or entered by the user.                                                                                               |
| MaximumQuantity                       | This field displays, for parts with a purchase method of min/max, the maximum quantity that the given part will be restocked to when it reaches the minimum quantity.                                    |
| IsMDIControlled                       | This field displays whether the given parts inventory record is controlled by MDI, as indicated on the OEM Control tab in the Parts Inventory application.                                               |
| MinimumQuantity                       | This field displays, for parts with a purchase method of min/max, the minimum quantity at which the given part will be restocked.                                                                        |
| OrderFrequency                        | This field displays at what frequency orders are, or can be, placed for the given part.                                                                                                                  |
| OrderPoint                            | This field displays the order point for the given part, as indicated on the purchase control tab in the part record.                                                                                     |
| OverrideProductClass                  | This field displays the override product class, if one exists, for the given part.                                                                                                                       |
| PartNumber                            | This field displays the part number of the given part.                                                                                                                                                   |
| PartType                              | This field displays whether the given part is a part, exchange, or core.                                                                                                                                 |
| Price1                                | This field displays the level 1, or highest, price for the given part.                                                                                                                                   |
| Price2                                | This field displays the level 2 price for the given part.                                                                                                                                                |
| Price3                                | This field displays the level 3 price for the given part.                                                                                                                                                |
| Price4                                | This field displays the level 4 price for the given part.                                                                                                                                                |
| Price5                                | This field displays the level 5 price for the given part.                                                                                                                                                |
| Price6                                | This field displays the level 6 price for the given part.                                                                                                                                                |
| Price7                                | This field displays the level 7, or lowest, price for the given part.                                                                                                                                    |
| PriceFileFactor                       | This field displays the divisor to be used to convert the unit of measure from the price file for the given part to the resale unit of measure for the given part.                                       |
| PriceFilePartNumber                   | This field displays the part number from the manufacturer on the price file for the given part, if it differs from the part number of the part in Fusion.                                                |
| PriceFileSource                       | This field displays the name of the price file for the given part.                                                                                                                                       |
| PriceFileSourceDescription            | This field displays a description of the price file for the given part.                                                                                                                                  |
| PriceGroup                            | This field displays the price group that the given part is associated with.                                                                                                                              |
| IsPriceUpdatedDuringReceiving         | This field displays whether the price of the given part is updated at the time of receiving.                                                                                                             |
| IsPrintLabel                          | This field displays whether an option will be available to print a label for the given part when it is added to a parts order.                                                                           |
| ProductCharacteristic                 | This field displays additional information about the given part number, intended to supplement the Alternate Description field.                                                                          |
| PurchaseConversion                    | This field displays the multiplier to be used to convert the selling unit of measure to the purchasing unit of measure from the vendor for the given part.                                               |
| PurchaseMethod                        | This field displays the purchase method associated with the given part, which determines at what point the part will be restocked.                                                                       |
| PurchUnitofMeasure                    | This field displays the unit of measure in which the given part is purchased from the vendor.                                                                                                            |
| QuantityAvailable                     | This field displays the quantity of the given part available to be sold.                                                                                                                                 |
| QuantityCommitted                     | This field displays the quantity of the given part that has been added to open parts or repair orders.                                                                                                   |
| QuantityOnBackOrder                   | This field displays the quantity of the given part that has been ordered by a customer but is not currently available in inventory.                                                                      |
| QuantityOnOrder                       | This field displays the quantity of the given part that has been ordered from vendors, but is not available in inventory yet.                                                                            |
| ReplacementCost                       | This field displays the replacement cost of the given part.                                                                                                                                              |
| ReturnCode                            | This field displays the return code associated with the given part.                                                                                                                                      |
| SafetyStockPercent                    | This field displays the percentage that the order point should be padded with when determining whether to restock the given part.                                                                        |
| Seasonal                              | This field displays whether the given part is considered seasonal, or 80% of the sales occur in six or fewer consecutive months.                                                                         |
| SellPackage                           | This field displays the package size in which the given part is sold to customers.                                                                                                                       |
| SellingUnitOfMeasure                  | This field displays the unit of measure in which the given part is sold to the customer.                                                                                                                 |
| SerialStockType                       | This field displays whether a serial number is required for the given part (No indicates that it is not required, Point of Sale indicates that it will be required at the point of sale).                |
| StockClass                            | This field displays the stock class of the given part.                                                                                                                                                   |
| StockStatus                           | This field displays the stock status of the given part.                                                                                                                                                  |
| SupersedePriceFilePartNumber          | This field displays the part number in the price file that the given part has superseded to.                                                                                                             |
| SupplierCode                          | This field displays the supplier code of the supplier for the given part.                                                                                                                                |
| SupplierBuyPackage                    | This field displays the quantity in which the given part is purchased from the supplier.                                                                                                                 |
| TariffNumber                          | This field displays the tariff number associated with the given part.                                                                                                                                    |
| UpdateFromPriceFile                   | This field displays whether the pricing of the given part is updated via price file.                                                                                                                     |
| VelocityCode                          | This field displays the velocity code associated with the given part.                                                                                                                                    |
| Weight                                | This field displays the weight of the given part.                                                                                                                                                        |
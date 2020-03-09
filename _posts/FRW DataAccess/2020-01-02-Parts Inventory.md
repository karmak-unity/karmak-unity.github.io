---
layout: post
title: "Branch Inventory"
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

 <!-- 


 -->  <hr>Field Details...

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

 <!-- 


 -->  <hr>Field Details...

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

---
---
### Branch Inventory Usage
---

This data object is used to display usage of a given parts inventory detail
record. A record will be displayed for each month/year combination in which the
given part had greater than zero picks or greater than zero sales. Please note
that no records will be displayed for a part that has never had any picks or
sales. To get a listing of all parts inventory records with their corresponding
usage records, start in Parts Inventory or Parts Inventory Extended and join to
Parts Inventory Usage.

This information comes from the 12 Month History tab in the Parts Inventory
application in Fusion.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**            | **Column Description**                                                                                                                                                             |
|---|---|
| AverageCost                   | This field displays the average cost of the given part.                                                                                                                            |
| BarCode                       | This field displays the bar code for the given parts inventory detail record.                                                                                                      |
| BinLocation                   | This field displays the bin location for the given parts inventory detail record.                                                                                                  |
| Branch                        | This field displays the branch associated with the given parts inventory detail record.                                                                                            |
| DateAdded                     | This field displays the date on which the given part was added to inventory, from the Dates group box on the Purchase Control tab in the parts inventory record.                   |
| DaysSinceLastSale             | This field displays the number of days between the last sold date and the current date.                                                                                            |
| Description                   | This field displays the description of the given part.                                                                                                                             |
| Ignore                        | This field displays whether the automatically recorded picks and usage for the given month were marked to be ignored for reporting and ordering purposes.                          |
| Inactive                      | This field displays whether the given parts inventory detail record has been marked as inactive.                                                                                   |
| LastCountDate                 | This field displays the date on which the given part was last counted, from the Dates group box on the Purchase Control tab in the parts inventory record.                         |
| LastOrderedDate               | This field displays the date on which the given part was last ordered, from the Dates group box on the Purchase Control tab in the parts inventory record.                         |
| LastOutOfStockDate            | This field displays the date on which the given part last went out of stock, from the Dates group box on the Purchase Control tab in the parts inventory record.                   |
| LastPriceChangeDate           | This field displays the date on which the price of the given part was last changed, from the Dates group box on the Purchase Control tab in the parts inventory record.            |
| LastPriceFileUpdate           | This field displays the date on which the price file for the given part was last updated, from the Dates group box on the Purchase Control tab in the parts inventory record.      |
| LastReceivedDate              | This field displays the date on which the given part was last received, from the Dates group box on the Purchase Control tab in the parts inventory record.                        |
| LastReplacementCostChangeDate | This field displays the date on which the replacement cost of the given part was last changed, from the Dates group box on the Purchase Control tab in the parts inventory record. |
| LastSoldDate                  | This field displays the date on which the given part was last sold, from the Dates group box on the Purchase Control tab in the parts inventory record.                            |
| LIFODate                      | This field displays the LIFO date for the given part, from the Dates group box on the Purchase Control tab in the parts inventory record.                                          |
| LostSales                     | This field displays the number of lost sales that were recorded for the given part in the given month and year.                                                                    |
| ManualPicks                   | This field displays the number of picks that were manually recorded on the 12 Month History tab for the given part and the given month and year.                                   |
| ManualSales                   | This field displays the number of sales that were manually recorded on the 12 Month History tab for the given part and the given month and year.                                   |
| Month                         | This field displays the month in which the picks and usage displayed in the given record occurred.                                                                                 |
| PartNumber                    | This field displays the part number of the given part.                                                                                                                             |
| PartType                      | This field displays the part type of the given part.                                                                                                                               |
| Picks                         | This field displays the number of picks that were recorded by the application for the given part in the given month and year.                                                      |
| PYPicks                       | This field displays the total number of picks for the given part in the year prior to the given year.                                                                              |
| PYSales                       | This field displays the total number of sales for the given part in the year prior to the given year.                                                                              |
| PYTDPicks                     | This field displays the number of picks for the given part through the given month in the year prior to the given year.                                                            |
| PYTDSales                     | This field displays the number of sales for the given part through the given month in the year prior to the given year.                                                            |
| QuantityAvailable             | This field displays the quantity available of the given part at the given branch.                                                                                                  |
| QuantityCommitted             | This field displays the quantity of the given part at the given branch that is committed to open orders.                                                                           |
| QuantityOnBackorder           | This field displays the quantity of the given part at the given branch that is on backorder from invoiced orders.                                                                  |
| QuantityOnOrder               | This field displays the quantity of the given part at the given branch that is expected from open purchase orders.                                                                 |
| ReplacementCost               | This field displays the replacement cost of the given part.                                                                                                                        |
| Sales                         | This field displays the number of sales that were recorded by the application for the given part in the given month and year.                                                      |
| StockClass                    | This field displays the stock class of the given part.                                                                                                                             |
| StockStatus                   | This field displays the stock status for the given parts inventory detail record.                                                                                                  |
| Supplier                      | This field displays the supplier associated with the given part.                                                                                                                   |
| TotalLostSales                | This field displays the total lost sales for the given part in the given month and year, from the Total Lost column on the 12 Month History tab.                                   |
| TotalPicks                    | This field displays the total picks (Picks + Manual Picks) for the given part and the given month and year.                                                                        |
| TotalSales                    | This field displays the total sales (Sales + Manual Sales) for the given part and the given month and year.                                                                        |
| Year                          | This field displays the year in which the picks and usage displayed in the given record occurred.                                                                                  |
| YTDPicks                      | This field displays the number of picks for the given part through the given month in the given year.                                                                              |
| YTDSales                      | This field displays the number of sales for the given part through the given month in the given year.                                                                              |


---
---
### Parts Inventory Usage Trailing 12 Months
---

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**         | **Column Description** |
|---|---|
| AprManualPicks             |                        |
| AprManualSales             |                        |
| AprPicks                   |                        |
| AprSales                   |                        |
| AprTotalPicks              |                        |
| AprTotalSales              |                        |
| AugManualPicks             |                        |
| AugManualSales             |                        |
| AugPicks                   |                        |
| AugSales                   |                        |
| AugTotalPicks              |                        |
| AugTotalSales              |                        |
| Branch                     |                        |
| CurrentMonth               |                        |
| CurrentMonthManualPicks    |                        |
| CurrentMonthManualSales    |                        |
| CurrentMonthPicks          |                        |
| CurrentMonthSales          |                        |
| CurrentMonthTotalPicks     |                        |
| CurrentMonthTotalSales     |                        |
| CurrentYear                |                        |
| DateAdded                  |                        |
| DecManualPicks             |                        |
| DecManualSales             |                        |
| DecPicks                   |                        |
| DecSales                   |                        |
| DecTotalPicks              |                        |
| DecTotalSales              |                        |
| FebManualPicks             |                        |
| FebManualSales             |                        |
| FebPicks                   |                        |
| FebSales                   |                        |
| FebTotalPicks              |                        |
| FebTotalSales              |                        |
| JanManualPicks             |                        |
| JanManualSales             |                        |
| JanPicks                   |                        |
| JanSales                   |                        |
| JanTotalPicks              |                        |
| JanTotalSales              |                        |
| JulManualPicks             |                        |
| JulManualSales             |                        |
| JulPicks                   |                        |
| JulSales                   |                        |
| JulTotalPicks              |                        |
| JulTotalSales              |                        |
| JunManualPicks             |                        |
| JunManualSales             |                        |
| JunPicks                   |                        |
| JunSales                   |                        |
| JunTotalPicks              |                        |
| JunTotalSales              |                        |
| MarManualPicks             |                        |
| MarManualSales             |                        |
| MarPicks                   |                        |
| MarSales                   |                        |
| MarTotalPicks              |                        |
| MarTotalSales              |                        |
| MayManualPicks             |                        |
| MayManualSales             |                        |
| MayPicks                   |                        |
| MaySales                   |                        |
| MayTotalPicks              |                        |
| MayTotalSales              |                        |
| NovManualPicks             |                        |
| NovManualSales             |                        |
| NovPicks                   |                        |
| NovSales                   |                        |
| NovTotalPicks              |                        |
| NovTotalSales              |                        |
| OctManualPicks             |                        |
| OctManualSales             |                        |
| OctPicks                   |                        |
| OctSales                   |                        |
| OctTotalPicks              |                        |
| OctTotalSales              |                        |
| PartNumber                 |                        |
| SepManualPicks             |                        |
| SepManualSales             |                        |
| SepPicks                   |                        |
| SepSales                   |                        |
| SepTotalPicks              |                        |
| SepTotalSales              |                        |
| SuggestedOrderMonths       |                        |
| Supplier                   |                        |
| Trailing12MonthManualPicks |                        |
| Trailing12MonthManualSales |                        |
| Trailing12MonthPicks       |                        |
| Trailing12MonthSales       |                        |
| Trailing12MonthTotalPicks  |                        |
| Trailing12MonthTotalSales  |                        |


---
---
### Parts Inventory Yearly Usage
---

This data object is used to display parts inventory picks and sales by month for
each year in which the given part has had picks or sales. Please note that if
there were no picks or sales in a given year, there will be no record for that
year. The data is displayed with a row for each year and a column for each
month. Please note that the 13 Month fields only contain data for the current
year's records, summarizing the past 13 months.

This information can be found in the Parts Inventory application in Fusion,
largely on the 12 Month History tab.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**   | **Column Description**                                                                                                                                                                                                                                                                                               |
|---|---|
| 13MonthLostSales     | This field displays, for the current year records, the lost sales for the given part for the past 13 months (current month + last 12 months).                                                                                                                                                                        |
| 13MonthManualPicks   | This field displays, for the current year records, the manual picks for the given part for the past 13 months (current month + last 12 months).                                                                                                                                                                      |
| 13MonthManualSales   | This field displays, for the current year records, the manual sales for the given part for the past 13 months (current month + last 12 months).                                                                                                                                                                      |
| 13MonthPicks         | This field displays, for the current year records, the picks for the given part for the past 13 months (current month + last 12 months).                                                                                                                                                                             |
| 13MonthSales         | This field displays, for the current year records, the sales for the given part for the past 13 months (current month + last 12 months).                                                                                                                                                                             |
| 13MonthTotalPicks    | This field displays, for the current year records, the total picks (picks + manual picks) for the given part for the past 13 months (current month + last 12 months).                                                                                                                                                |
| 13MonthTotalSales    | This field displays, for the current year records, the total sales (sales + manual sales) for the given part for the past 13 months (current month + last 12 months).                                                                                                                                                |
| AprManualPicks       | This field displays the quantity of picks manually recorded for the given part for April of the given year.                                                                                                                                                                                                          |
| AprManualSales       | This field displays the quantity of sales manually recorded for the given part for April of the given year.                                                                                                                                                                                                          |
| AprPicks             | This field displays quantity of picks for the given part in the month of April in the given year.                                                                                                                                                                                                                    |
| AprSales             | This field displays quantity of sales for the given part in the month of April in the given year.                                                                                                                                                                                                                    |
| AprTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for April of the given year.                                                                                                                                                                                                           |
| AprTotalSales        | This field displays the total sales (sales + manual sales) for the given part for April of the given year.                                                                                                                                                                                                           |
| AugManualPicks       | This field displays the quantity of picks manually recorded for the given part for August of the given year.                                                                                                                                                                                                         |
| AugManualSales       | This field displays the quantity of sales manually recorded for the given part for August of the given year.                                                                                                                                                                                                         |
| AugPicks             | This field displays quantity of picks for the given part in the month of August in the given year.                                                                                                                                                                                                                   |
| AugSales             | This field displays quantity of sales for the given part in the month of August in the given year.                                                                                                                                                                                                                   |
| AugTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for August of the given year.                                                                                                                                                                                                          |
| AugTotalSales        | This field displays the total sales (sales + manual sales) for the given part for August of the given year.                                                                                                                                                                                                          |
| BarCode              | This field displays the barcode associated with the given part.                                                                                                                                                                                                                                                      |
| BinLocation          | This field displays the bin location associated with the given part.                                                                                                                                                                                                                                                 |
| Branch               | This field displays the branch that the given part record is associated with.                                                                                                                                                                                                                                        |
| DateAdded            | This field displays the date on which the given part was added to inventory, from the Purchase Control tab in the Parts Inventory application. Please note that this date can be manually updated in Fusion, so it could differ from the system generated add date on the bottom of the Parts Inventory application. |
| DecManualPicks       | This field displays the quantity of picks manually recorded for the given part for December of the given year.                                                                                                                                                                                                       |
| DecManualSales       | This field displays the quantity of sales manually recorded for the given part for December of the given year.                                                                                                                                                                                                       |
| DecPicks             | This field displays quantity of picks for the given part in the month of December in the given year.                                                                                                                                                                                                                 |
| DecSales             | This field displays quantity of sales for the given part in the month of December in the given year.                                                                                                                                                                                                                 |
| DecTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for December of the given year.                                                                                                                                                                                                        |
| DecTotalSales        | This field displays the total sales (sales + manual sales) for the given part for December of the given year.                                                                                                                                                                                                        |
| Description          | This field displays the description associated with the given part number.                                                                                                                                                                                                                                           |
| FebManualPicks       | This field displays the quantity of picks manually recorded for the given part for February of the given year.                                                                                                                                                                                                       |
| FebManualSales       | This field displays the quantity of sales manually recorded for the given part for February of the given year.                                                                                                                                                                                                       |
| FebPicks             | This field displays quantity of picks for the given part in the month of February in the given year.                                                                                                                                                                                                                 |
| FebSales             | This field displays quantity of sales for the given part in the month of February in the given year.                                                                                                                                                                                                                 |
| FebTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for February of the given year.                                                                                                                                                                                                        |
| FebTotalSales        | This field displays the total sales (sales + manual sales) for the given part for February of the given year.                                                                                                                                                                                                        |
| Inactive             | This field displays whether the given part has been set to inactive.                                                                                                                                                                                                                                                 |
| JanManualPicks       | This field displays the quantity of picks manually recorded for the given part for January of the given year.                                                                                                                                                                                                        |
| JanManualSales       | This field displays the quantity of sales manually recorded for the given part for January of the given year.                                                                                                                                                                                                        |
| JanPicks             | This field displays quantity of picks for the given part in the month of January in the given year.                                                                                                                                                                                                                  |
| JanSales             | This field displays quantity of sales for the given part in the month of January in the given year.                                                                                                                                                                                                                  |
| JanTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for January of the given year.                                                                                                                                                                                                         |
| JanTotalSales        | This field displays the total sales (sales + manual sales) for the given part for January of the given year.                                                                                                                                                                                                         |
| JulManualPicks       | This field displays the quantity of picks manually recorded for the given part for July of the given year.                                                                                                                                                                                                           |
| JulManualSales       | This field displays the quantity of sales manually recorded for the given part for July of the given year.                                                                                                                                                                                                           |
| JulPicks             | This field displays quantity of picks for the given part in the month of July in the given year.                                                                                                                                                                                                                     |
| JulSales             | This field displays quantity of sales for the given part in the month of July in the given year.                                                                                                                                                                                                                     |
| JulTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for July of the given year.                                                                                                                                                                                                            |
| JulTotalSales        | This field displays the total sales (sales + manual sales) for the given part for July of the given year.                                                                                                                                                                                                            |
| JunManualPicks       | This field displays the quantity of picks manually recorded for the given part for June of the given year.                                                                                                                                                                                                           |
| JunManualSales       | This field displays the quantity of sales manually recorded for the given part for June of the given year.                                                                                                                                                                                                           |
| JunPicks             | This field displays quantity of picks for the given part in the month of June in the given year.                                                                                                                                                                                                                     |
| JunSales             | This field displays quantity of sales for the given part in the month of June in the given year.                                                                                                                                                                                                                     |
| JunTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for June of the given year.                                                                                                                                                                                                            |
| JunTotalSales        | This field displays the total sales (sales + manual sales) for the given part for June of the given year.                                                                                                                                                                                                            |
| MarManualPicks       | This field displays the quantity of picks manually recorded for the given part for March of the given year.                                                                                                                                                                                                          |
| MarManualSales       | This field displays the quantity of sales manually recorded for the given part for March of the given year.                                                                                                                                                                                                          |
| MarPicks             | This field displays quantity of picks for the given part in the month of March in the given year.                                                                                                                                                                                                                    |
| MarSales             | This field displays quantity of sales for the given part in the month of March in the given year.                                                                                                                                                                                                                    |
| MarTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for March of the given year.                                                                                                                                                                                                           |
| MarTotalSales        | This field displays the total sales (sales + manual sales) for the given part for March of the given year.                                                                                                                                                                                                           |
| MayManualPicks       | This field displays the quantity of picks manually recorded for the given part for May of the given year.                                                                                                                                                                                                            |
| MayManualSales       | This field displays the quantity of sales manually recorded for the given part for May of the given year.                                                                                                                                                                                                            |
| MayPicks             | This field displays quantity of picks for the given part in the month of May in the given year.                                                                                                                                                                                                                      |
| MaySales             | This field displays quantity of sales for the given part in the month of May in the given year.                                                                                                                                                                                                                      |
| MayTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for May of the given year.                                                                                                                                                                                                             |
| MayTotalSales        | This field displays the total sales (sales + manual sales) for the given part for May of the given year.                                                                                                                                                                                                             |
| NovManualPicks       | This field displays the quantity of picks manually recorded for the given part for November of the given year.                                                                                                                                                                                                       |
| NovManualSales       | This field displays the quantity of sales manually recorded for the given part for November of the given year.                                                                                                                                                                                                       |
| NovPicks             | This field displays quantity of picks for the given part in the month of November in the given year.                                                                                                                                                                                                                 |
| NovSales             | This field displays quantity of sales for the given part in the month of November in the given year.                                                                                                                                                                                                                 |
| NovTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for November of the given year.                                                                                                                                                                                                        |
| NovTotalSales        | This field displays the total sales (sales + manual sales) for the given part for November of the given year.                                                                                                                                                                                                        |
| OctManualPicks       | This field displays the quantity of picks manually recorded for the given part for October of the given year.                                                                                                                                                                                                        |
| OctManualSales       | This field displays the quantity of sales manually recorded for the given part for October of the given year.                                                                                                                                                                                                        |
| OctPicks             | This field displays quantity of picks for the given part in the month of October in the given year.                                                                                                                                                                                                                  |
| OctSales             | This field displays quantity of sales for the given part in the month of October in the given year.                                                                                                                                                                                                                  |
| OctTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for October of the given year.                                                                                                                                                                                                         |
| OctTotalSales        | This field displays the total sales (sales + manual sales) for the given part for October of the given year.                                                                                                                                                                                                         |
| PartNumber           | This field displays the part number of the given part record.                                                                                                                                                                                                                                                        |
| PartType             | This field displays the part type (Part, Exchange, or Core) of the given part.                                                                                                                                                                                                                                       |
| SepManualPicks       | This field displays the quantity of picks manually recorded for the given part for September of the given year.                                                                                                                                                                                                      |
| SepManualSales       | This field displays the quantity of sales manually recorded for the given part for September of the given year.                                                                                                                                                                                                      |
| SepPicks             | This field displays quantity of picks for the given part in the month of September in the given year.                                                                                                                                                                                                                |
| SepSales             | This field displays quantity of sales for the given part in the month of September in the given year.                                                                                                                                                                                                                |
| SepTotalPicks        | This field displays the total picks (picks + manual picks) for the given part for September of the given year.                                                                                                                                                                                                       |
| SepTotalSales        | This field displays the total sales (sales + manual sales) for the given part for September of the given year.                                                                                                                                                                                                       |
| StockStatus          | This field displays the stock status of the given part.                                                                                                                                                                                                                                                              |
| SuggestedOrderMonths | This field displays the months of sales history that should be considered when making decisions about purchasing for the given part.                                                                                                                                                                                 |
| Supplier             | This field displays the supplier of the given parts inventory record.                                                                                                                                                                                                                                                |
| Year                 | This field displays the year in which the given part usage was recorded.                                                                                                                                                                                                                                             |


---
---
### Parts Physical Inventory
---

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**                   | **Column Description**                                                                                                                                                                                                                                                                     |
|---|---|
| AddDate                              | This field will be the date the Physical Inventory or Cycle Count was created via Request Physical Inventory.                                                                                                                                                                              |
| AddUser                              | This field will be the Fusion username who created the Physical Inventory or Cycle Count via Request Physical Inventory.                                                                                                                                                                   |
| AverageCostDifference                | This field is a dollar value that represents the extended dollar amount difference between the new and old quantity of all parts on the Physical Inventory or Cycle Count. This is represented based on the Average Cost and when the Average Cost is blank Replacement Cost will be used. |
| Branch                               | This field is the Branch Code that the Physical Inventory or Cycle Count was done in.                                                                                                                                                                                                      |
| IsCompleted                          | This field identifies whether the Cycle Count has been completed or not. Valid options will be Yes or No and this will be set to completed when the Physical Inventory or Cycle Count has been finalized in Physical Inventory Update                                                      |
| CoreOptions                          | This field will display what the Cores Group Box was set to at the time the Physical Inventory or Cycle Count was created via Request Physical Inventory. Valid options will be Include, Exclude or Cores Only.                                                                            |
| DateCompleted                        | This field will identify the date that the Physical Inventory or Cycle Count was completed. This value will be the same as the Last Update Date when the Is Completed value is set to Yes.                                                                                                 |
| EndingBinLocation                    | This field identifies the Ending Bin Location that was entered at the time the Physical Inventory or Cycle Count was requested.                                                                                                                                                            |
| EndingLastCountedDate                | This field identifies the Ending Last Counted Date from the Part Inventory Detail record that was used to filter results at the time the Physical Inventory or Cycle Count was requested.                                                                                                  |
| EndingLastReceivedDate               | This field identifies the Ending Last Received Date from the Part Inventory Detail record that was used to filter results at the time the Physical Inventory or Cycle Count was requested.                                                                                                 |
| EndingLastSoldDate                   | This field identifies the Ending Last Sold Date from the Part Inventory Detail record that was used to filter results at the time the Physical Inventory or Cycle Count was requested.                                                                                                     |
| EndingPartNumber                     | This field identifies the Ending Part Number that was entered at the time the Physical Inventory or Cycle Count was requested.                                                                                                                                                             |
| EndingSupplier                       | This field identifies the Ending Supplier that was entered at the time the Physical Inventory or Cycle Count was requested.                                                                                                                                                                |
| ExcludeItemsWithZeroAvailable        | This field identifies whether the Exclude Items with Zero Available option was set to Yes or No at the time the Physical Inventory or Cycle Count was created.                                                                                                                             |
| IsFullInventory                      | This field identifies whether the Is Full Inventory option was set to Yes or No at the time the Physical Inventory or Cycle Count was created.                                                                                                                                             |
| LastUpdateDate                       | This field will be the date the Physical Inventory or Cycle Count was last updated via Request Physical Inventory.                                                                                                                                                                         |
| LastUpdateUser                       | This field will be the Fusion username who last updated the Physical Inventory or Cycle Count via Request Physical Inventory.                                                                                                                                                              |
| NumberOfWriteInLinesPerPage          | This field is the number of write in lines per page that were used at the time the Physical Inventory or Cycle Count was created.                                                                                                                                                          |
| PageBreak                            | This field identifies the Page Break of the Physical Inventory or Cycle Count. Valid options are None or Bin Location.                                                                                                                                                                     |
| PageBreakPosition                    | This field identifies the Page Break Position of the Physical Inventory or Cycle Count                                                                                                                                                                                                     |
| PartCount                            | This field is a count of all parts that were on the Physical Inventory or Cycle Count. This will include Write In Parts.                                                                                                                                                                   |
| PrintAlternateBinLocations           | This field identifies whether the Print Alternate Bin Locations option was set to Yes or No at the time the Physical Inventory or Cycle Count was created.                                                                                                                                 |
| PrintDetailOfQuantityCommitted       | This field identifies whether the Print Detail of Quantity Committed option was set to Yes or No at the time the Physical Inventory or Cycle Count was created.                                                                                                                            |
| PrintQuantityAvailable               | This field identifies whether the Print Quantity Available option was set to Yes or No at the time the Physical Inventory or Cycle Count was created.                                                                                                                                      |
| PrintQuantityCommitted               | This field identifies whether the Print Quantity Committed option was set to Yes or No at the time the Physical Inventory or Cycle Count was created.                                                                                                                                      |
| PrintSequence                        | This field identifies the Print Sequence of the Physical Inventory or Cycle Count. Valid options are Bin Location or Supplier/Part Number.                                                                                                                                                 |
| ReplacementCostDifference            | This field is a dollar value that represents the extended dollar amount difference between the new and old quantity of all parts on the Physical Inventory or Cycle Count. This is represented based on the Replacement Cost.                                                              |
| RequireMaintenanceUpdateOnAllRecords | This field identifies whether the Require Maintenance Update on All Records option was set to Yes or No at the time the Physical Inventory or Cycle Count was created.                                                                                                                     |
| SetCountQuantitytoZero               | This field identifies whether the Set Count Quantity to Zero option was set to Yes or No at the time the Physical Inventory or Cycle Count was created.                                                                                                                                    |
| StartingBinLocation                  | This field identifies the Starting Bin Location that was entered at the time the Physical Inventory or Cycle Count was requested.                                                                                                                                                          |
| StartingLastCountedDate              | This field identifies the Starting Last Counted Date from the Part Inventory Detail record that was used to filter results at the time the Physical Inventory or Cycle Count was requested.                                                                                                |
| StartingLastReceivedDate             | This field identifies the Starting Last Received Date from the Part Inventory Detail record that was used to filter results at the time the Physical Inventory or Cycle Count was requested.                                                                                               |
| StartingLastSoldDate                 | This field identifies the Starting Last Sold Date from the Part Inventory Detail record that was used to filter results at the time the Physical Inventory or Cycle Count was requested.                                                                                                   |
| StartingPartNumber                   | This field identifies the Starting Part Number that was entered at the time the Physical Inventory or Cycle Count was requested.                                                                                                                                                           |
| StartingSupplier                     | This field identifies the Starting Supplier that was entered at the time the Physical Inventory or Cycle Count was requested.                                                                                                                                                              |
| WriteInCount                         | This field is a count of all Write In Parts that were on the Physical Inventory or Cycle Count.                                                                                                                                                                                            |


---
---
### Parts Physical Inventory Detail
---

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**          | **Column Description**                                                                                                                                                                                                                                                |
|---|---|
| AddDate                     | This field will be the date the Physical Inventory or Cycle Count request was created. If the detail part is a write in line, it will be date the write in line was added.                                                                                            |
| AddUser                     | This field will be the user who created the Physical Inventory or Cycle Count request. If the detail part is a write in line, it will be the user who added the write in line.                                                                                        |
| AverageCost                 | This field is the Average cost of the detail part record on the Physical Inventory or Cycle Count request. If this part is an Exchange Part, it will be the cost of the Exchange Part + Inherent Core. If the Average Cost is blank this will be the Replacement Cost |
| AverageCostDifference       | This field is the difference in average cost between the extended replacement cost of the new and old quantities of the detail part record on the Physical Inventory or Cycle Count request. If the average cost is blank the replacement cost will be used.          |
| InherentCoreAverageCost     | This file is the Average Cost of the Inherent Core of the detail part record on the Physical Inventory or Cycle Count request. If the Average Cost is blank this will be the replacement cost.                                                                        |
| InherentCoreReplacementCost | This file is the Replacement Cost of the Inherent Core of the detail part record on the Physical Inventory or Cycle Count request.                                                                                                                                    |
| LastUpdateDate              | This field will be the date the specific detail part was last updated on the Physical Inventory or Cycle Count request was created.                                                                                                                                   |
| LastUpdateUser              | This field will be the user who last updated the specific detail part record on the Physical Inventory or Cycle Count request.                                                                                                                                        |
| NewQuantity                 | This field is the quantity that was entered for the part detail record at the time the specific Physical Inventory or Cycle Count was finalized.                                                                                                                      |
| OldQuantity                 | This field is the Quantity Available of the part detail record at the time the specific Physical Inventory or Cycle Count was requested.                                                                                                                              |
| PartDescription             | This field displays the description of the given part record.                                                                                                                                                                                                         |
| PartNumber                  | This field displays the part number for the specific Physical Inventory or Cycle Count requested record.                                                                                                                                                              |
| IsProcessed                 | This field will indicate whether the part detail record has been processed on the specific Physical Inventory or Cycle Count request. The valid values are Yes or No.                                                                                                 |
| QuantityDifference          | This field is the difference between the New Quantity and Old Quantity of the detail part record on the Physical Inventory or Cycle Count request.                                                                                                                    |
| ReplacementCost             | This field is the Replacement cost of the detail part record on the Physical Inventory or Cycle Count request. If this part is an Exchange Part, it will be the cost of the Exchange Part + Inherent Core.                                                            |
| ReplacementCostDifference   | This field is the difference in replacement cost between the extended replacement cost of the new and old quantities of the detail part record on the Physical Inventory or Cycle Count request.                                                                      |
| Sequence                    | This field is the sequence number of the part detail record for the specific Physical Inventory or Cycle Count request.                                                                                                                                               |
| Supplier                    | This field identifies the supplier associated with the given part record.                                                                                                                                                                                             |
| IsWriteIn                   | This field will indicate whether the part detail record that is entered on the specific Physical Inventory or Cycle Count request was a write in line or not. The valid values are Yes or No.                                                                         |


---
---
### Parts Alternate Bin Locations
---

This data object displays the alternate bin associated with a part record, if
one exists.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**   | **Column Description**                                                                     |
|---|---|
| AddDate              | This field displays the date on which the bin location was added to the part.              |
| AddUser              | This field displays the user name that added the record.                                   |
| AlternateBinLocation | This field displays the alternate bin location of the part.                                |
| Branch               | This field displays the branch associated with the part number.                            |
| LastUpdate           | This field displays the date on which an A/P invoice was last updated.                     |
| UpdateUser           | This field displays the user name of the individual who made the update.                   |
| PartNumber           | This field displays the part number of a part on a miscellaneous purchase order.           |
| Sequence             | This field displays the order in which the alternate bins for a given part number display. |

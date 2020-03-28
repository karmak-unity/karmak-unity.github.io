---
layout: post
title: "Parts Inventory Usage"
category: "Parts" 
icon: "icon-gear"
type: "data_access" comments: falsedescription:  Access to usage of a given parts inventory detail record.
---

---
---

This data object is used to display usage of a given parts inventory detail record. A record will be displayed for each month/year combination in which the given part had greater than zero picks or greater than zero sales. Please note that no records will be displayed for a part that has never had any picks or sales. To get a listing of all parts inventory records with their corresponding usage records, start in Parts Inventory or Parts Inventory Extended and join to Parts Inventory Usage. 

This information comes from the 12 Month History tab in the Parts Inventory application in Fusion.

 #### URL 
```
/frw/PartsInventoryUsage
``` 
<hr>Field Details...

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
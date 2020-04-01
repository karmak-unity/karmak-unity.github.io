---
layout: post
title: "Parts Inventory Yearly Usage"
category: "Parts" 
icon: "icon-gear"
type: "data_access" 
comments: false
description:  Access to display parts inventory picks and sales by month for each year in which the given part has had picks or sales.
---

---
---

This data object is used to display parts inventory picks and sales by month for each year in which the given part has had picks or sales. Please note that if there were no picks or sales in a given year, there will be no record for that year. The data is displayed with a row for each year and a column for each month. Please note that the 13 Month fields only contain data for the current year's records, summarizing the past 13 months.

This information can be found in the Parts Inventory application in Fusion, largely on the 12 Month History tab.

 
#### URL 
```
/frw/PartsInventoryYearlyUsage
``` 

<hr>
Field Details...

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
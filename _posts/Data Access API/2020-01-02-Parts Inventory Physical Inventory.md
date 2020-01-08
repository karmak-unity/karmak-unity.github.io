---
layout: post
title: "Parts Physical Inventory"
category: "Parts" 
icon: "icon-gear"
type: "data_access" comments: falsedescription:  Access to physical inventory available within the Fusion system
---

---
---
### Parts Physical Inventory
---

 <!-- SQL VIEW:  **vwIN_SSR_PartsPhysicalInventory**



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

 <!-- SQL VIEW:  **vwIN_SSR_PartsPhysicalInventoryDetail**



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

 <!-- SQL VIEW:  **vwIN_SSR_PartsAlternateBinLocations**



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
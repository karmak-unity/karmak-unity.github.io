---
layout: post
title: "Parts Physical Inventory Detail"
category: "Parts" 
icon: "icon-gear"
type: "data_access" 
comments: false
description:  Access to physical inventory detail information within Fusion
---

---
---

 
#### URL 
```
/frw/PartsPhysicalInventoryDetail
``` 
 <hr>
Field Details...

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
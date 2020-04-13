---
layout: post
title: "Repair Order Detail"
category: "Repair Order"
icon: "icon-wrench"
type: "data_access" 
comments: false
description: Access all detail information about Open and Invoiced Repair Orders. 
---
 
---
---

This data object is used to display all part, labor, and miscellaneous charge detail items on a given repair order.

This information can be found in the Repair Order application within the Fusion business system.

#### URL
```
/frw/RepairOrderDetails
```
 
<hr>
Field Details...

| **SQL Field Name**       | **Column Description**                                                                                                                                                                               |
|---|---|
| AddDate                  | This field displays the date on which the given repair order detail item was added.                                                                                                                  |
| AddUser                  | This field displays the user name of the user who added the given repair order detail item.                                                                                                          |
| AverageCost              | This field displays the cost or average cost or, if average cost is zero, the replacement cost of the given repair order detail item.                                                                |
| BackorderPriority        | This field displays the backorder priority flag that was entered when the given part for which backorder was necessary was added to the repair order.                                                |
| BillCustomerOT           | This field displays whether the customer will be billed extra for overtime hours on the given repair order.                                                                                          |
| IsBillingAdjustment      | This field displays whether the labor hours on the repair order have been adjusted for billing.                                                                                                      |
| BillingCompanyName       | This field displays the company name of the billing customer on the given repair order.                                                                                                              |
| BillingCustomer          | This field displays the customer number of the billing customer on the given repair order.                                                                                                           |
| BinLocation              | This field displays the bin location of the given part on the repair order.                                                                                                                          |
| Branch                   | This field displays the branch in which the given repair order was created.                                                                                                                          |
| CalculatedAgainst        | This field displays which value the specified percentage is applied to in order to determine the price of the given miscellaneous charge on the repair order.                                        |
| CalculatedPrice          | This field displays the price of the given detail item before override price is taken into consideration.                                                                                            |
| ControlNumber            | This field displays the control number associated with the part or miscellaneous charge.                                                                                                             |
| CoreClass                | This field displays the class of the core for the given exchange part.                                                                                                                               |
| CoreCost                 | This field displays the cost of the core for the given exchange part.                                                                                                                                |
| CoreDescription          | This field displays the description of the core for the given exchange part.                                                                                                                         |
| CoreExtendedPrice        | This field displays the extended price (price \* quantity) of the core for the given exchange part.                                                                                                  |
| IsCoreNoCharge           | This field displays whether the core for the given exchange part was added to the repair order at no charge.                                                                                         |
| IsCoreOneLineTransaction | This field displays whether the given exchange part and its core will appear as one line with a single transaction on the repair order.                                                              |
| CoreOverridePrice        | This field displays the override price entered for the core for the given exchange part at the time it was added to the repair order.                                                                |
| CorePartNumber           | This field displays the part number of the core for the given exchange part.                                                                                                                         |
| CorePrice                | This field displays the price of the core for the given exchange part.                                                                                                                               |
| CoreReferenceMPO         | This field displays the reference MPO associated with the core for the given exchange part.                                                                                                          |
| CoreSupplier             | This field displays the supplier of the core for the given exchange part.                                                                                                                            |
| Department               | This field displays the department in which the given repair order was created.                                                                                                                      |
| Division                 | This field displays the division in which the given repair order was created.                                                                                                                        |
| EHCCharge                | This field displays the total amount for the environmental handling charge on the given repair order.                                                                                                |
| EHCCode                  | This field displays the code for the environmental handling charge added to the given part on the repair order.                                                                                      |
| EHCDescription           | This field displays the description of the environmental handling charge added to the given part on the repair order.                                                                                |
| IsEnterLaborInTotalHours | This field displays whether the quantity of hours on the given labor task were entered manually as a lump sum, rather than calculated by the times at which the technician clocked in and out.       |
| ExtendedAverageCost      | This field displays the extended average cost (average cost \* quantity) of the given repair order detail item.                                                                                      |
| Extended Price           | This field displays the extended price (price \* quantity or hourly rate \* quantity) of the given repair order detail item.                                                                         |
| ExtendedReplacementCost  | This field displays the extended replacement cost (replacement cost \* quantity) of the given repair order detail item.                                                                              |
| ExtendedSellingCost      | This field displays the extended selling cost (selling cost \* quantity) of the given repair order detail item.                                                                                      |
| FillingBranch            | This field displays the filling branch of the given part on the repair order.                                                                                                                        |
| InsideSalesperson        | This field displays the user name of the salesperson responsible for the sale of the given part on the repair order.                                                                                 |
| DateInvoiced             | This field displays the date on which the given repair order was invoiced.                                                                                                                           |
| InvoiceNumber            | This field displays the invoice number of the given invoiced repair order.                                                                                                                           |
| Item                     | This field displays the part number, technician number, or an identifying description of the given repair order detail item.                                                                         |
| ItemDescription          | This field displays a description of the given repair order detail item.                                                                                                                             |
| KitAssemblyTemplate      | This field displays an indicator of whether the part is a kit, assembly, or template. Note that this field is not used in Fusion at this time.                                                       |
| LastUpdateDate           | This field displays the date on which the given repair order detail item was last updated.                                                                                                           |
| LastUpdateUser           | This field displays the user name of the user who last updated the given repair order detail item.                                                                                                   |
| Message                  | This field displays the message entered at the time the part or miscellaneous charge was added to the repair order.                                                                                  |
| Method                   | This field displays the method, manual or percentage, of the given miscellaneous charge on the repair order.                                                                                         |
| IsNoCharge               | This field displays whether the given part detail record was added to the repair order at no charge.                                                                                                 |
| OEMPrice                 | This field displays the customer's selling price of the part that was received from the OEM in a price verification.                                                                                 |
| OEMRebateAmount          | This field displays the rebate amount received from the OEM in a price verification that the cost of the transaction can be reduced by.                                                              |
| OTBillingTotal           | This field displays the total amount that will be billed as overtime (OT Hours \* OT Hourly Rate) on the given labor task.                                                                           |
| OTDescription            | This field displays the description of the overtime multiplier associated with the overtime hours on the given labor task.                                                                           |
| OTHourlyCost             | This field displays the hourly cost of the overtime hours associated with the given labor task.                                                                                                      |
| OTHourlyRate             | This field displays the hourly rate of the overtime hours associated with the given labor task.                                                                                                      |
| OTHours                  | This field displays the number of labor hours on the repair order that are considered overtime.                                                                                                      |
| OTMultiplier             | This field displays the multiplier used to determine cost per hour for overtime hours.                                                                                                               |
| OutsideSalesperson       | This field displays the outside parts salesperson associated with the customer on the given repair order.                                                                                            |
| OverridePrice            | This field displays the override price entered for the given detail item when it was added to the repair order (Parts and Misc Charges, at the time of input. Labor, at the time of task creation.). |
| OverrideTaxStatus        | This field displays the override tax status entered for the part or miscellaneous charge at the time it was added to the repair order.                                                               |
| OwningCompanyName        | This field displays the company name of the owning customer on the given repair order.                                                                                                               |
| OwningCustomer           | This field displays the customer number of the owning customer on the given repair order.                                                                                                            |
| PartActionFlag           | This field displays the part action flag selected when the given repair order detail item was selected to be added to the repair order.                                                              |
| PartStockNumber          | This field displays the stock number of the given part, which is used to uniquely identify a part that is tracked by serial number. Note that this field is not used in Fusion at this time.         |
| PartTechnician           | This field displays the technician associated with the given part on the repair order.                                                                                                               |
| PartType                 | This field displays the part type of the given part.                                                                                                                                                 |
| IsPartialFill            | This field displays whether the given part detail record on the repair order was partially filled.                                                                                                   |
| Percentage               | This field displays the percentage that is applied to a specified value to determine the price of the given miscellaneous charge on the repair order.                                                |
| IsPolicyAdjustment       | This field displays whether the given part on the repair order is for policy adjustment.                                                                                                             |
| Price                    | This field displays the price at which the given detail item was sold (Override Price if there is one, Calculated Price if not).                                                                     |
| ProductClass             | This field displays the product class associated with the given miscellaneous charge on the repair order.                                                                                            |
| ProductCode              | This field displays the product code associated with the given part, which indicates user defined groups of parts.                                                                                   |
| IsPulled                 | This field displays whether the given part was pulled from inventory for the given repair order.                                                                                                     |
| QuantityHours            | This field displays the quantity of the given repair order detail item included on the repair order.                                                                                                 |
| RateLevelDescription     | This field displays the description of the labor rate being used for billing on the overtime hours associated with the given labor task.                                                             |
| ReferenceMPO             | This field displays the reference MPO associated with the part or miscellaneous charge.                                                                                                              |
| RepairGroup              | This field displays the repair group associated with the given labor task.                                                                                                                           |
| RepairType               | This field displays the repair type associated with the given labor task.                                                                                                                            |
| ReplacementCost          | This field displays the cost or replacement cost of the given repair order detail item.                                                                                                              |
| RONumber                 | This field displays the repair order number of the given repair order.                                                                                                                               |
| ROStatus                 | This field displays the current status of the given repair order.                                                                                                                                    |
| SerialNumber             | This field displays the serial number of the given part on the repair order.                                                                                                                         |
| SerialStockType          | This field displays the serial stock type associated with the given part on the repair order.                                                                                                        |
| Shift                    | This field displays the shift code for the given technician.                                                                                                                                         |
| Supplier                 | This field displays the supplier of the given part.                                                                                                                                                  |
| TaskNumber               | This field displays the task number that the given repair order detail item is associated with.                                                                                                      |
| TimeIn                   | This field displays the date and time at which the technician clocked in.                                                                                                                            |
| TimeOut                  | This field displays the date and time at which the technician clocked out.                                                                                                                           |
| TransactionType          | This field displays the transaction type for the given repair order detail item.                                                                                                                     |
| UnitNumber               | This field displays the unit number of the unit that is being serviced on the given repair order.                                                                                                    |
| UnitOfMeasure            | This field displays the units in which the given part on the repair order is sold.                                                                                                                   |
| StockNumber              | This field displays the stock number of the unit that is being serviced on the given repair order.                                                                                                   |
| IsWarranty               | This field displays whether the given part on the repair order is considered warranty.                                                                                                               |
| Weight                   | This field displays the weight of the given part on the repair order.                                                                                                                                |

---
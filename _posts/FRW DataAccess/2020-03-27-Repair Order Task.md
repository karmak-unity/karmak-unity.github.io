---
layout: post
title: "Repair Order Task"
category: "Repair Order"
icon: "icon-wrench"
type: "data_access" 
comments: false
description: Access to show all repair order task information
---
 
---
---

This data object is used to show all repair order task information.

This information can be found in the Repair Order program within the Fusion business system.

#### URL
```
/frw/RepairOrderTask
```

<HR>

Field Details...

| **SQL Field Name**           | **Column Description**                                                                                                                                                    |
|---|---|
| AlternateBillingCompanyName  | This field displays the company name of the alternate billing customer assigned to the task if one exists.                                                                |
| AlternateBillingCustomer     | This field displays the alternate billing customer assigned to the task if one exists.                                                                                    |
| BillToCompanyName            | This field displays the company name of the Bill To Customer the repair order was opened under.                                                                           |
| BillToCustomer               | This field displays the customer number of the Bill To Customer the repair order was opened under.                                                                        |
| Branch                       | This field displays the branch associated with the repair order.                                                                                                          |
| IsTaskAComebackRepair        | This field displays whether or not a task is a comeback repair                                                                                                            |
| Department                   | This field displays the department associated with a Repair Order.                                                                                                        |
| Division                     | This field displays the company division the Repair order associated with the given task was opened under.                                                                |
| InvoiceDate                  | This field displays the date on which the invoice was created.                                                                                                            |
| InvoiceNumber                | This field displays the invoice number the given task was invoiced on.                                                                                                    |
| TaskLastUpdateUser           | This field displays the User who last updated the RO Task for the specific instance of the RO.                                                                            |
| OwningCompanyName            | This field displays the company name of the Owning Customer the repair order was opened under.                                                                            |
| OwningCustomer               | This field displays the customer number of the Owning customer the repair order was opened under.                                                                         |
| RONumber                     | This field displays the Repair order number the given task is associated with.                                                                                            |
| TaskAddDate                  | This field displays the Add Date of the RO Task for the specific instance of the RO.                                                                                      |
| TaskAddUser                  | This field displays the User who added the RO Task for the specific instance of the RO.                                                                                   |
| TaskAdjustmentTime           | This field displays the total amount of hours on the task flagged as a billing adjustment.                                                                                |
| TaskAlwaysPayBillingHours    | This field indicates whether or not the technicians who worked on the task will always be paid the billing hours worked on the given task.                                |
| TaskBillingHours             | This field displays the number of hours that will be billed to a customer for a particular task.                                                                          |
| TaskBookHours                | This field displays the estimated amount of time it will take to perform a task.                                                                                          |
| TaskCallBackDays             | This field displays the number of days allowed for comeback that has been assigned to the given Repair Order Task.                                                        |
| TaskCauseComment             | This field displays the cause comment entered for the given task.                                                                                                         |
| IsTaskClockedON              | This field displays whether or not a technician is clocked on the given task.                                                                                             |
| TaskClockedOnTechnicians     | This field displays the names and associated numbers of any technicians currently clocked on to a repair order task.                                                      |
| TaskComebackReason           | This field displays the reason that a task was flagged for comeback.                                                                                                      |
| TaskComplaintComment         | This field displays the complaint comment entered for the given task.                                                                                                     |
| IsTaskCompleted              | This field displays whether or not a task is completed.                                                                                                                   |
| TaskCloseDate                | This field displays the date on which the given task was completed.                                                                                                       |
| TaskCorrectionComment        | This field displays the correction comment entered for the given task.                                                                                                    |
| TaskDefaultLaborRate         | This field displays the original labor rate to be charged on a given repair order task.                                                                                   |
| TaskDepartment               | This field displays the department associated with a repair order task.                                                                                                   |
| TaskEffectiveLaborRate       | This field displays the given tasks effective labor rate (Task total labor divided by hours worked).                                                                      |
| TaskEHCCharge                | This field displays the total amount of EHC charges that have been added to the given task.                                                                               |
| TaskHoursBilled              | This field displays the total hours billed for the given Task.                                                                                                            |
| TaskHoursWorked              | This field displays the total number of hours worked on any one task (Note if three technicians worked on one task, this would be the number of hours between the three). |
| TaskLaborAccounting          | This field displays the alternate labor accounting that has been assigned to the given task.                                                                              |
| TaskLaborActual              | This field displays the total extended price of all labor charges on the given task that are not flagged as billing adjustments.                                          |
| TaskLaborCost                | This field displays the total cost of all labor charges on the given task.                                                                                                |
| TaskLaborQuote               | This field displays the quoted amount for Labor charges assigned to the given repair order task.                                                                          |
| TaskLaborRate                | This field displays the labor rate associated with a task.                                                                                                                |
| TaskLaborRateCode            | This field displays the labor rate code assigned to the given task.                                                                                                       |
| TaskLaborRateDescription     | This field displays the description of the labor rate code assigned to the given task.                                                                                    |
| TaskLastUpdateDate           | This field displays the Last Update Date of the RO Task for the specific instance of the RO.                                                                              |
| TaskMiscellaneousCharges     | This field displays the total extended price of all miscellaneous charges that have been added to the given repair task.                                                  |
| TaskMiscellaneousChargesCost | This field displays the total cost of all miscellaneous charges added to the given repair task.                                                                           |
| TaskNumber                   | This field displays the number attached to a given task.                                                                                                                  |
| TaskOpenTime                 | This field displays the sum of all open time transactions for the given repair order task.                                                                                |
| TaskOverrideLaborRate        | This field displays the labor rate override to be charged on a given repair order task.                                                                                   |
| TaskOverrideTaxStatus        | This field displays the override tax status that has been assigned to the given task.                                                                                     |
| TaskPartsAccounting          | This field displays the alternate parts accounting that has been assigned to the given task.                                                                              |
| TaskPartsAverageCost         | This field displays the total average cost of all parts that have been added to the given repair order task.                                                              |
| TaskPartsQuote               | This field displays the quoted amount for parts for the given repair order task.                                                                                          |
| TaskPartsReplacementCost     | This field displays the total replacement cost of all parts on a repair order task.                                                                                       |
| TaskPartsSellingCost         | This field displays the selling cost of all parts that have been added to the given repair order task.                                                                    |
| TaskRemainingHours           | This field displays the number of hours remaining for the given repair order task.                                                                                        |
| TaskRepairGroup              | This field displays the repair group assigned to a task.                                                                                                                  |
| TaskRepairGroupDescription   | This field displays the description of a given repair group.                                                                                                              |
| TaskRepairType               | This field displays the Repair Type assigned to the given Repair Order Task.                                                                                              |
| TaskRepairTypeDescription    | This field displays the description of the Repair Type assigned to the given task.                                                                                        |
| TaskSRTCode                  | This field displays the vendor's SRT code associated with a task, if any.                                                                                                 |
| TaskStatus                   | This field displays the status of the given task.                                                                                                                         |
| TaskTechnicians              | This field displays the names and numbers of any technicians who are or have been clocked on to a specific task of a repair order.                                        |
| TaskTotal                    | This field diplays the total price of all charges added to the given task.                                                                                                |
| TaskTotalActual              | This field displays the total extended price of all charges add to the given task, less and charge flagged as a billing adjustment.                                       |
| TaskTotalAverageCost         | This field displays the total average cost of all charges that have been added to the given repair order task.                                                            |
| TaskTotalCost                | This field displays the total cost of all charges added to the given task.                                                                                                |
| TaskTotalLabor               | This field displays the total extended price of all labor charges on the given task.                                                                                      |
| TaskTotalParts               | This field displays the total extended price of all parts charges on the given task.                                                                                      |
| TaskTotalReplacementCost     | This field displays the total replacement cost of a all charges that have been added to the given repair order task.                                                      |
| TaskTotalSellingCost         | This field displays the total of all parts selling cost on a particular repair task.                                                                                      |
| TaskTotalTimeWorked          | This field displays the total amount of hours worked on the given task  not including billing adjustments.                                                                |
| TaskUseBookHours             | This field displays whether or not the given task is flagged to use book hours instead of billing hours.                                                                  |
| IsTaskWaiting                | This field displays "Yes" if a repair order is not flagged as completed and no one is currently clocked on.                                                               |
| IsTaskWaitingForParts        | This field displays whether or not the given task is waiting for parts.                                                                                                   |
| UnitNumber                   | This field displays the Unit number assigned to the repair order the given task is associated with.                                                                       |
| VMRSCode                     | This field displays the VMRS Code that has been assigned to the given Repair Order Task.                                                                                  |
| VMRSCodeDescription          | This field displays the description of the VMRS Code that has been assigned to the given Repair Order Task.                                                               |
| VMRSFailure                  | This field displays the VMRS failure description the user has assigned to the given repair order task.                                                                    |
| VMRSReason                   | This field displays the VMRS reason description the user has assigned to the given repair order task.                                                                     |
| VMRSTask                     | This field displays the VMRS Task description that has been assigned to the given Repair Order Task.                                                                      |
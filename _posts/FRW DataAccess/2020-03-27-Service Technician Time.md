---
layout: post
title: "Service Technician Time"
category : "Service Technician"
icon: "icon-man"
type: "data_access" 
comments: false
description: Access to display all completed technician time records
---

---
---


This data object is used to display all completed technician time records.

This information can be found in the Technician Time Search and the Time Entry Search applications in the Fusion business system.

#### URL
```
/frw/TechnicianTime
``` 

<hr>
Field Details...

| **SQL Field Name**               | **Column Description**                                                                                                                                     |
|---|---|
| AddApplication | This field displays the name of the application in Fusion that the given technician time record was created from. | 
| AddApplicationNumber | This field displays the identifying code of the application in Fusion that the given technician time record was created from. | 
| AddDate | This field displays the date on which the given technician time record was created in Fusion. | 
| AddUser | This field displays the username of the user that created the given technician time record in Fusion. | 
| BarcodeDateIn | This field displays the punch in date for the given technician time transaction. | 
| BarcodeDateOut | This field displays the punch out date for the given technician time transaction. | 
| BarcodeTimeIn | This field displays the punch in time for the given technician time transaction. | 
| BarcodeTimeOut | This field displays the punch out time for the given technician time transaction. | 
| IsBase | This field displays whether the given technician time transaction occurred at the base location and during the base shift for the given technician. | 
| OT_BillCustomer | This field displays whether the customer will be billed at an overtime rate for any overtime hours that occurred in the given technician time transaction. | 
| TotalHours | This field displays the total hours for the given billable time transaction. | 
| IsBillingAdjustment | This field displays whether the given time transaction is a billing adjustment. | 
| BillingCompanyName | This field displays the company name of the billing customer associated with the repair order on the given time transaction. | 
| BillingCustomer | This field displays the customer number of the billing customer associated with the repair order on the given time transaction. | 
| BillingHours | This field displays the billing hours for the task that the given technician time record is associated with. | 
| BranchCode | This field displays the branch in which the given time transaction occurred. | 
| ClockOutReason | This field will indicate the reason the Technician clocked out of a Repair Order or Non-Billable Repair Type when not clocking directly into another Repair Order or Non-Billable Repair Type. Valid options are blank, Off or any value setup in SVM97900 Clock Out Reason that get associated with the specific time transaction. | 
| CombinedTotalHours | This field displays the total hours for the given time transaction, whether it is billable or nonbillable. | 
| IsCompleted | This field displays whether the given time transaction has been completed. | 
| Cost | This field displays the unit cost of the given time transaction. | 
| Department | This field displays the department in which the given time transaction occurred. | 
| IsEnterLaborInTotalHours | This field displays whether the given time transaction was entered as total hours, rather than using the punch in/out fields. | 
| ExtendedCost | This field displays the total cost of the given time transaction. | 
| ExtendedPrice | This field displays the total price of the given time transaction. | 
| HoursBilled | This field displays the number of hours billed for the given time transaction. | 
| HoursWorked | This field displays the number of hours that were actively worked for the given time transaction. | 
| IsInOutTime | This field displays whether the given time transaction was entered using the punch in/out fields, rather than as total hours. | 
| InvoiceNumber | This field displays the invoice number of the repair order that the given time transaction is associated with. | 
| Invoiced | This field displays whether the repair order that the given time transaction is associated with has been invoiced. | 
| LaborQuote | This field displays the labor quote assigned to the task that the given time transaction is associated with. | 
| LaborRate | This field displays the hourly rate associated with the given time transaction. | 
| LaborRateCode | This field displays the identifying code for the labor rate associated with the given time transaction. | 
| LastUpdate | This field displays the date on which the given technician time record was last updated in Fusion. | 
| UpdateUser | This field displays the username of the user that last updated the given technician time record in Fusion. | 
| IsManuallyUpdated | This field displays whether the given time transaction has been updated outside of Barcode Time Transactions. | 
| IsNonBillable | This field displays whether the given time transaction is nonbillable. | 
| NBExtendedCost | This field displays the total cost of the nonbillable hours in the given time transaction. | 
| NBOT_TotalCost | This field displays the total cost of the nonbillable overtime hours in the given time transaction. | 
| NBOT_TotalHours | This field displays the number of nonbillable hours that are considered overtime in the given time transaction. | 
| NBTotalHours | This field displays the total hours for the given nonbillable time transaction. | 
| OriginalRepairOrder | This field displays the repair order number of the repair order that the given repair order was spun off from. | 
| OTBillingTotal | This field displays the total price of the overtime hours in the given time transaction. | 
| OT_Cost | This field displays the cost of the hours in the given time transaction that are considered overtime. | 
| OT_RateMultLevelParamNum | This field displays the cost level for the hours in the given time transaction that are considered overtime. | 
| OTHourlyRate | This field displays the price per hour for the overtime hours in the given time transaction. | 
| OT_RateLevelParamNum | This field displays the rate level for the overtime hours in the given time transaction. | 
| OT_RateMultiplier | This field displays the rate multiplier for the hours in the given time transaction that are considered overtime. | 
| OT_TotalHours | This field displays the total number of hours in the given time transaction that are considered overtime. | 
| OwningCompanyName | This field displays the company name of the owning customer associated with the repair order on the given time transaction. | 
| OwningCustomer | This field displays the customer number of the owning customer associated with the repair order on the given time transaction. | 
| IsPayrollProcessed | This field displays whether the given time transaction has been processed through payroll. | 
| IsPolicyAdjustmentTransaction | This field displays whether the given time transaction is a policy adjustment. | 
| Price | This field displays the unit price of the given time transaction. | 
| RepairGroup | This field displays the repair group that the given time transaction and repair task are associated with. | 
| RepairGroupDescription | This field displays the description of the repair group that the given time transaction and repair task are associated with. | 
| RepairOrderNumber | This field displays repair order number that the given time transaction is associated with. | 
| RepairOrderStatus | This field displays the status of the repair order that the given time transaction is associated with. | 
| RepairTaskStatus | This field displays the status of the repair task that the given time transaction is associated with. | 
| RepairType | This field displays the repair type of the task that the given time transaction is associated with. | 
| RepairTypeDescription | This field displays the description of the repair type of the task that the given time transaction is associated with. | 
| IsReversal | This will field will display Yes or No depending on whether the Non-Billable Technician Time Transaction record being displayed was created as a reversing entry based on the user using the Void option in Technician Time Maintenance for on a Non-Billable Technician Time Transaction | 
| IsSecondaryRO | This field displays whether the given time transaction is associated with a secondary repair order. | 
| Shift | This field displays the shift during which the given time transaction occurred. | 
| IsSubmittedforPayroll | This field displays whether the given time transaction has been submitted to payroll. | 
| TaskNumber | This field displays the task number on the repair order that the given time transaction is associated with. | 
| TechnicianFirstName | This field displays the first name of the technician for the given time transaction. | 
| TechnicianLastName | This field displays the last name of the technician for the given time transaction. | 
| TechnicianName | This field displays the full name of the technician for the given time transaction. | 
| TechnicianNumber | This field displays the technician number of the technician for the given time transaction. | 
| TotalHoursLessBillingAdjustments | This field displays the total hours, without counting billing adjustments, for the given billable time transaction. | 
| TotalOTCost | This field displays the total cost of the overtime hours in the given time transaction. | 
| UpdateApplication | This field displays the name of the application in Fusion that the given technician time record was last updated from. | 
| UpdateApplicationNumber | This field displays the identifying code of the application in Fusion that the given technician time record was last updated from. | 
| UseBookHours | This field displays whether the given task is indicated to be billed based on book hours, rather than billing hours. | 
| IsVoided | This field will display Yes or No depending on whether a Non-Billable Technician Time Transaction recorded being displayed has been voided in Fusion. | 
| IsWarrantyTransaction | This field displays whether the task that the given time transaction is associated with is a warranty transaction. | 


---
layout: post
title: "Service Technician"
category : "Service Technician"
icon: "icon-man"
type: "data_access" comments: falsedescription: Access to view all service technician information
---

---
---
### Technician Information
---

This data object is used to show all service technician information.

This information can be found in the Technician program within the Fusion business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**       | **Column Description**                                                                                                 |
|---|---|
| AddDate                  | This field displays the date and time the technician was added to the system.                                          |
| AddUser                  | This field displays username that added the technician to the sytem.                                                   |
| DoNotPayOvertime         | This field displays whether or not the techincian will be paid overtime when they work beyond the regular work period. |
| IsFlatRate               | This field displays whether or not a technician is paid a flat rate.                                                   |
| HireDate                 | This field displays the date on which a technician was hired.                                                          |
| Inactive                 | This field displays whether or not a given technician is set to inactive.                                              |
| LastUpdate               | This field displays the date and time the record was last updated.                                                     |
| LastUpdateUser           | This field displays the username that last updated the record.                                                         |
| HoursPerDayBeforeOT      | This field displays the maximum hours per day a technician will work without charging over time.                       |
| HoursPerWeekBeforeOT     | This field displays the maximum hours per week a technician will work without charging over time.                      |
| IsPayIncentive           | This field displays whether or not a technician receives an incentive or not.                                          |
| RatePerHour              | This field displays the rate per hour a technician charges.                                                            |
| ReviewDate               | This field indicates when the next or last review date for the technician should be or should have happened.           |
| ShiftPremium             | This field displays the additional pay a specific shift will earn.                                                     |
| IsTechnicianAvailable    | This field shows if the technician is clocked on a job.                                                                |
| TechnicianBaseBranch     | This field displays the technician's main branch location.                                                             |
| TechnicianBaseDepartment | This field displays the department associated with a repair order task, if any.                                        |
| TechnicianBaseShift      | This field displays the shift code for a technician, if any.                                                           |
| TechnicianName           | This field displays the technician's name.                                                                             |
| TechnicianNumber         | This field displays the number assigned to a technician.                                                               |

---
---
### Service Technician Certification
---

This data object is used to display all technician certificate information.

This information can be found in the Technician and Technician Certification
Type programs within the Fusion business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**            | **Column Description**                                                              |
|---|---|
| AddDate                       | This field displays the date and time of when ther record was added to they system. |
| Add User                      | This field displays the user name that added the record.                            |
| Certification Date            | This field displays the date on which the technician was certified.                 |
| Certification Description     | This field displays the description of the certification.                           |
| Certification Expiration Date | This field displays the date on which the technician's certification will expire.   |
| Certification Type            | This field displays the type of certification the technician has.                   |
| LastUpdateDate                | This field displays the date and time the records was last updated.                 |
| Update User                   | This field displays the user who last updated the file.                             |
| IsPermit                      | This field displays whether or not a certification is a permit.                     |
| IsPrintOnInvoice              | This field displays whether or not the certification prints on an invoice.          |
| Tech Certification Number     | This field displays the number assigned to a technician for their certifications.   |
| Technician Name               | This field displays the technician's name.                                          |
| Technician Number             | This field displays the number assigned to a technician.                            |

---
---
### Service Technician Performance
---

This data object is used to display technician performance by repair group.

This information can be found in the Technician application within the Fusion
business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**         | **Column Description**                                                                                                                                                     |
|---|---|
| BeginningCalculationDate   | This field displays the date on which performance for the given technician and associated repair group was first calculated to be greater than zero.                       |
| ComebackHours              | This field displays the total number of hours that have had to be worked on repairs after the given technician initially serviced them.                                    |
| EffectiveLaborRate         | This field displays the effective labor rate ((Billed Hours \* Labor Rate)/Productive Hours) for the given technician and repair group.                                    |
| EfficiencyFreezeThruDate   | This field displays the date through which the efficiency calculation for the given technician and associated repair group will be frozen.                                 |
| EfficiencyPercentage       | This field displays the efficiency of the given technician for the given repair group as a percentage, from the Performance tab of the Technician application in Fusion.   |
| GainLossFreezeThruDate     | This field displays the date through which the gain loss calculation for the given technician and associated repair group will be frozen.                                  |
| GainLossPercentage         | This field displays the gain loss of the given technician for the given repair group as a percentage, from the Performance tab of the Technician application in Fusion.    |
| HireDate                   | This field displays the date on which the given technician was hired.                                                                                                      |
| Inactive                   | This field displays whether the given technician has been marked as inactive in Fusion.                                                                                    |
| LastCalculationDate        | This field displays the most recent date on which performance was calculated for the given technician and associated repair group.                                         |
| PaidFlatRate               | This field displays whether the given technician is paid with a flat rate.                                                                                                 |
| PaidIncentive              | This field displays whether the pay for the given technician is affected by incentive bonuses.                                                                             |
| ProductivityFreezeThruDate | This field displays the date through which the productivity calculation for the given technician and associated repair group will be frozen.                               |
| ProductivityPercentage     | This field displays the productivity of the given technician for the given repair group as a percentage, from the Performance tab of the Technician application in Fusion. |
| ProficiencyFreezeThruDate  | This field displays the date through which the proficiency calculation for the given technician and associated repair group will be frozen.                                |
| ProficiencyPercentage      | This field displays the proficiency of the given technician for the given repair group as a percentage, from the Performance tab of the Technician application in Fusion.  |
| RepairGroup                | This field displays the repair group code that the given technician performance values are associated with.                                                                |
| RepairGroupDescription     | This field displays the description of the repair group that the given technician performance values are associated with.                                                  |
| ReviewDate                 | This field displays the most current past review date or scheduled review date for the given technician.                                                                   |
| TechnicianBaseBranch       | This field displays the base branch location for the given technician.                                                                                                     |
| TechnicianBaseDepartment   | This field displays the base department location for the given technician.                                                                                                 |
| TechnicianBaseShift        | This field displays the base shift time for the given technician.                                                                                                          |
| TechnicianName             | This field displays the name (first, middle initial, last) of the given technician.                                                                                        |
| TechnicianNumber           | This field displays the identifying code for the given technician.                                                                                                         |
| TechnicianUserName         | This field displays the username for the given technician in Fusion.                                                                                                       |

---
---
### Service Technician Productivity
---

This data object is used to display how productive a technician has been,
summarized by month.

This information can be found in the Technician program within the Fusion
business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**       | **Column Description**                                                                                                                                          |
|---|---|
| BilledHours              | This field displays the total number of hours billed for the given month/year combiniation.                                                                     |
| ComebackHours            | This field displays the total number of comeback hours a technician has worked for the given month/year combination.                                            |
| EffectiveRate            | This field displays the technician's effective rate for the given month/year combiniation (Billed Hours \* Labor Rate / Productive Hours).                      |
| EfficiencyPercentage     | This field displays the technician's calculated efficiency percentage for the given month/year combination (Billed hours / Productive hours).                   |
| GainLossPercentage       | This field displays the technician's calculated gain/loss percentage for the given month/year combination (Billed hours / total hours worked).                  |
| Inactive                 | This field displays whether or not a given technician is set to inactive.                                                                                       |
| Month                    | This field displays the name of the month productivity figures are being displayed for.                                                                         |
| MonthNumber              | This field displays the month number producivity figures are being displayed for.                                                                               |
| NonProductiveHours       | This field displays the number of non productive hours a technician has worked for the given month/year combination.                                            |
| ProductiveHours          | This field displays the number of productive hours a technician has worked for the given month/year combination.                                                |
| ProductivityPercentage   | This field displays the technician's productivity percentage for the given month/year combination (Productive hours / total hours worked).                      |
| ProficiencyPercentage    | This field displays the technician's calculated proficiency percentage for the given month/year combination (Billed hours - comeback hours / productive hours). |
| TechnicianBaseBranch     | This field displays the technician's main branch location.                                                                                                      |
| TechnicianBaseDepartment | This field displays the given technician's base department.                                                                                                     |
| TechnicianBaseShift      | This field displays the shift assigned to the given technician.                                                                                                 |
| TechnicianName           | This field displays the technician's name.                                                                                                                      |
| TechnicianNumber         | This field displays the number assigned to a technician.                                                                                                        |
| TotalWorkedHours         | This field displays the technician's total hours worked for the given month/year combination (productive hours + non productive hours).                         |
| Year                     | This field displays the year productivity figures are being displayed for.                                                                                      |

---
---
### Service Technician Time
---

This data object is used to display all completed technician time records.

This information can be found in the Technician Time Search and the Time Entry
Search applications in the Fusion business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**               | **Column Description**                                                                                                                                     |
|---|---|
| AddApplication                   | This field displays the name of the application in Fusion that the given technician time record was created from.                                          |
| AddApplicationNumber             | This field displays the identifying code of the application in Fusion that the given technician time record was created from.                              |
| AddDate                          | This field displays the date on which the given technician time record was created in Fusion.                                                              |
| AddUser                          | This field displays the username of the user that created the given technician time record in Fusion.                                                      |
| BarcodeDateIn                    | This field displays the punch in date for the given technician time transaction.                                                                           |
| BarcodeDateOut                   | This field displays the punch out date for the given technician time transaction.                                                                          |
| BarcodeTimeIn                    | This field displays the punch in time for the given technician time transaction.                                                                           |
| BarcodeTimeOut                   | This field displays the punch out time for the given technician time transaction.                                                                          |
| IsBase                           | This field displays whether the given technician time transaction occurred at the base location and during the base shift for the given technician.        |
| OT_BillCustomer                  | This field displays whether the customer will be billed at an overtime rate for any overtime hours that occurred in the given technician time transaction. |
| TotalHours                       | This field displays the total hours for the given billable time transaction.                                                                               |
| IsBillingAdjustment              | This field displays whether the given time transaction is a billing adjustment.                                                                            |
| BillingCompanyName               | This field displays the company name of the billing customer associated with the repair order on the given time transaction.                               |
| BillingCustomer                  | This field displays the customer number of the billing customer associated with the repair order on the given time transaction.                            |
| BillingHours                     | This field displays the billing hours for the task that the given technician time record is associated with.                                               |
| BranchCode                       | This field displays the branch in which the given time transaction occurred.                                                                               |
| CombinedTotalHours               | This field displays the total hours for the given time transaction, whether it is billable or nonbillable.                                                 |
| IsCompleted                      | This field displays whether the given time transaction has been completed.                                                                                 |
| Cost                             | This field displays the unit cost of the given time transaction.                                                                                           |
| Department                       | This field displays the department in which the given time transaction occurred.                                                                           |
| IsEnterLaborInTotalHours         | This field displays whether the given time transaction was entered as total hours, rather than using the punch in/out fields.                              |
| ExtendedCost                     | This field displays the total cost of the given time transaction.                                                                                          |
| ExtendedPrice                    | This field displays the total price of the given time transaction.                                                                                         |
| HoursBilled                      | This field displays the number of hours billed for the given time transaction.                                                                             |
| HoursWorked                      | This field displays the number of hours that were actively worked for the given time transaction.                                                          |
| IsInOutTime                      | This field displays whether the given time transaction was entered using the punch in/out fields, rather than as total hours.                              |
| InvoiceNumber                    | This field displays the invoice number of the repair order that the given time transaction is associated with.                                             |
| Invoiced                         | This field displays whether the repair order that the given time transaction is associated with has been invoiced.                                         |
| LaborQuote                       | This field displays the labor quote assigned to the task that the given time transaction is associated with.                                               |
| LaborRate                        | This field displays the hourly rate associated with the given time transaction.                                                                            |
| LaborRateCode                    | This field displays the identifying code for the labor rate associated with the given time transaction.                                                    |
| LastUpdate                       | This field displays the date on which the given technician time record was last updated in Fusion.                                                         |
| UpdateUser                       | This field displays the username of the user that last updated the given technician time record in Fusion.                                                 |
| IsManuallyUpdated                | This field displays whether the given time transaction has been updated outside of Barcode Time Transactions.                                              |
| IsNonBillable                    | This field displays whether the given time transaction is nonbillable.                                                                                     |
| NBExtendedCost                   | This field displays the total cost of the nonbillable hours in the given time transaction.                                                                 |
| NBOT_TotalCost                   | This field displays the total cost of the nonbillable overtime hours in the given time transaction.                                                        |
| NBOT_TotalHours                  | This field displays the number of nonbillable hours that are considered overtime in the given time transaction.                                            |
| NBTotalHours                     | This field displays the total hours for the given nonbillable time transaction.                                                                            |
| OriginalRepairOrder              | This field displays the repair order number of the repair order that the given repair order was spun off from.                                             |
| OTBillingTotal                   | This field displays the total price of the overtime hours in the given time transaction.                                                                   |
| OT_Cost                          | This field displays the cost of the hours in the given time transaction that are considered overtime.                                                      |
| OT_RateMultLevelParamNum         | This field displays the cost level for the hours in the given time transaction that are considered overtime.                                               |
| OTHourlyRate                     | This field displays the price per hour for the overtime hours in the given time transaction.                                                               |
| OT_RateLevelParamNum             | This field displays the rate level for the overtime hours in the given time transaction.                                                                   |
| OT_RateMultiplier                | This field displays the rate multiplier for the hours in the given time transaction that are considered overtime.                                          |
| OT_TotalHours                    | This field displays the total number of hours in the given time transaction that are considered overtime.                                                  |
| OwningCompanyName                | This field displays the company name of the owning customer associated with the repair order on the given time transaction.                                |
| OwningCustomer                   | This field displays the customer number of the owning customer associated with the repair order on the given time transaction.                             |
| IsPayrollProcessed               | This field displays whether the given time transaction has been processed through payroll.                                                                 |
| IsPolicyAdjustmentTransaction    | This field displays whether the given time transaction is a policy adjustment.                                                                             |
| Price                            | This field displays the unit price of the given time transaction.                                                                                          |
| RepairGroup                      | This field displays the repair group that the given time transaction and repair task are associated with.                                                  |
| RepairGroupDescription           | This field displays the description of the repair group that the given time transaction and repair task are associated with.                               |
| RepairOrderNumber                | This field displays repair order number that the given time transaction is associated with.                                                                |
| RepairOrderStatus                | This field displays the status of the repair order that the given time transaction is associated with.                                                     |
| RepairTaskStatus                 | This field displays the status of the repair task that the given time transaction is associated with.                                                      |
| RepairType                       | This field displays the repair type of the task that the given time transaction is associated with.                                                        |
| RepairTypeDescription            | This field displays the description of the repair type of the task that the given time transaction is associated with.                                     |
| IsSecondaryRO                    | This field displays whether the given time transaction is associated with a secondary repair order.                                                        |
| Shift                            | This field displays the shift during which the given time transaction occurred.                                                                            |
| IsSubmittedforPayroll            | This field displays whether the given time transaction has been submitted to payroll.                                                                      |
| TaskNumber                       | This field displays the task number on the repair order that the given time transaction is associated with.                                                |
| TechnicianFirstName              | This field displays the first name of the technician for the given time transaction.                                                                       |
| TechnicianLastName               | This field displays the last name of the technician for the given time transaction.                                                                        |
| TechnicianName                   | This field displays the full name of the technician for the given time transaction.                                                                        |
| TechnicianNumber                 | This field displays the technician number of the technician for the given time transaction.                                                                |
| TotalHoursLessBillingAdjustments | This field displays the total hours, without counting billing adjustments, for the given billable time transaction.                                        |
| TotalOTCost                      | This field displays the total cost of the overtime hours in the given time transaction.                                                                    |
| UpdateApplication                | This field displays the name of the application in Fusion that the given technician time record was last updated from.                                     |
| UpdateApplicationNumber          | This field displays the identifying code of the application in Fusion that the given technician time record was last updated from.                         |
| UseBookHours                     | This field displays whether the given task is indicated to be billed based on book hours, rather than billing hours.                                       |
| IsWarrantyTransaction            | This field displays whether the task that the given time transaction is associated with is a warranty transaction.                                         |

---
layout: post
title: "Repair Order"
category: "Repair Order"
icon: "icon-wrench"
type: "data_access" 
---
 
---
---
### Service Repair Order Details
---

This data object is used to display all part, labor, and miscellaneous charge
detail items on a given repair order.

This information can be found in the Repair Order application within the Fusion
business system.

 



 

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
---
### Service Repair Order Header
---

This data object is used to display the header records for all repair orders in
Fusion, and contains one record for each order with summary information about
the repair order included. This data object can be joined to Repair Order Task
and then to Repair Order Details in order to view the detail information on the
repair order.

This information can be found in the repair order application in Fusion.

 



 

| **SQL Field Name**           | **Column Description**                                                                                                                                                                                |
|---|---|
| AddDate                      | This field displays the date on which the given repair order was added to the system.                                                                                                                 |
| ROServiceWriter              | This field displays, if available, the username of the user who created the given repair order or the username of the user who invoiced the given repair order.                                       |
| AuthorizationNumber          | This field displays the credit authorization number associated with the given repair order, from the billing customer tab in the repair order application.                                            |
| BillingContactname           | This field displays the name of the contact associated with the billing customer associated with the given repair order.                                                                              |
| BillingCustomerAccountStatus | This field displays the current status of the customer account for the billing customer associated with the given repair order.                                                                       |
| BillingCustomerAddress       | This field displays the street address of the billing customer associated with the given repair order.                                                                                                |
| BillingCustomerCity          | This field displays the city of the billing customer associated with the given repair order.                                                                                                          |
| BillingCustomerCountry       | This field displays the country of the billing customer associated with the given repair order.                                                                                                       |
| BillingCustomerCounty        | This field displays the county of the billing customer associated with the given repair order.                                                                                                        |
| BillingCustomerIndustryType  | This field displays the industry type of the billing customer associated with the given repair order.                                                                                                 |
| BillingCustomerName          | This field displays the company name of the billing customer associated with the given repair order.                                                                                                  |
| BillingCustomerNumber        | This field displays the customer number of the billing customer associated with the given repair order.                                                                                               |
| BillingCustomerPostalCode    | This field displays the postal code of the billing customer associated with the given repair order.                                                                                                   |
| BillingCustomerRegion        | This field displays the region of the billing customer associated with the given repair order.                                                                                                        |
| IsBillingCustomerWarranty    | This field displays whether the billing customer associated with the given repair order is a warranty customer.                                                                                       |
| BillingCustomerWorkPhone     | This field displays the work phone number for the billing customer associated with the given repair order.                                                                                            |
| BillingHomePhone             | This field displays the home phone number of the contact associated with the billing customer associated with the given repair order.                                                                 |
| Branch                       | This field displays the branch in which the given repair order was created.                                                                                                                           |
| CharacteristicType           | This field displays the characteristic type of the unit on the given repair order.                                                                                                                    |
| CompletedToInvoicedInterval  | This field displays the category the given repair order falls into based on the number of days that passed between completion and invoicing (00-01, 02-05, 06-10, 11-20, 21-30, 31-45, and 45+ days). |
| ContactHomePhone             | This field displays the home phone number of the contact associated with the unit owning customer associated with the given repair order.                                                             |
| ContactName                  | This field displays the name of the contact associated with the unit owning customer associated with the given repair order.                                                                          |
| ContactWorkPhone             | This field displays the work phone number of the contact associated with the unit owning customer associated with the given repair order.                                                             |
| CreditReserve                | This field displays the credit reserve amount associated with the given repair order.                                                                                                                 |
| CustomerAccountStatus        | This field displays the current status of the customer account for the unit owning customer associated with the given repair order.                                                                   |
| CustomerAddress              | This field displays the street address of the unit owning customer associated with the given repair order.                                                                                            |
| CustomerBaseBranch           | This field displays the base branch that the unit owning customer on the given repair order is associated with.                                                                                       |
| CustomerCity                 | This field displays the city of the unit owning customer associated with the given repair order.                                                                                                      |
| CustomerName                 | This field displays the company name of the unit owning customer associated with the given repair order.                                                                                              |
| CustomerNumber               | This field displays the customer number of the unit owning customer associated with the given repair order.                                                                                           |
| CustomerPhone                | This field displays the phone number for the unit owning customer associated with the given repair order.                                                                                             |
| CustomerPostalCode           | This field displays the postal code of the unit owning customer associated with the given repair order.                                                                                               |
| CustomerRegion               | This field displays the region of the unit owning customer associated with the given repair order.                                                                                                    |
| CustomerUnitNumber           | This field displays the unit number associated with the given repair order, owned by the unit owning customer.                                                                                        |
| IsCustomerWarranty           | This field displays whether the unit owning customer associated with the given repair order is a warranty customer.                                                                                   |
| DaysArrivalToFirstPunch      | This field displays the number of days between the arrival date on the repair order and the first time punch in on the repair order.                                                                  |
| DaysFirstPunchToLastPunch    | This field displays the number of days between the first time punch in and the last time punch out on the repair order.                                                                               |
| DaysOpenToFirstPunch         | This field displays the number of days between the open date on the repair order and the first time punch in on the repair order.                                                                     |
| Department                   | This field displays the department in which the given repair order was created.                                                                                                                       |
| Division                     | This field displays the division in which the given repair order was created.                                                                                                                         |
| ECMReading                   | This field displays the ECM meter reading recorded for the unit at the time of the given repair order.                                                                                                |
| EmailAddressOfCustomer       | This field displays the email address provided for the customer on the given repair order.                                                                                                            |
| FirstPunchDate               | This field displays the first time punch in on the repair order.                                                                                                                                      |
| FollowUpEmailFlag            | This field displays whether the given repair order requires a follow up email.                                                                                                                        |
| InServiceDate                | This field displays the date on which the given unit first went into service.                                                                                                                         |
| IndustryType                 | This field displays the industry type of the unit owning customer associated with the given repair order.                                                                                             |
| InvoiceDueDate               | This field displays the date on which the given repair order invoice is due to be paid.                                                                                                               |
| InvoiceNumber                | This field displays the invoice number of the given invoiced repair order.                                                                                                                            |
| InvoiceUser                  | This field displays the username of the user who invoiced the given repair order.                                                                                                                     |
| LastPunchDate                | This field displays the last time punch out on the repair order.                                                                                                                                      |
| LastUpdate                   | This field displays the date on which the given repair order was last updated in the system.                                                                                                          |
| UpdateUser                   | This field displays the username of the user who last updated the given repair order.                                                                                                                 |
| LPONumber                    | This field displays the local purchase order number associated with the given repair order.                                                                                                           |
| MeterType                    | This field displays the unit of measure associated with the meter reading for the unit on the given repair order.                                                                                     |
| OriginalRONumber             | This field displays the repair order number from the original repair order for repair orders that were created from another repair order, as a spinoff.                                               |
| PaymentMethod                | This field displays the method by which the repair order will be paid by the billing customer.                                                                                                        |
| RemoteApplication            | This field displays the name of the remote application that the given repair order was created by.                                                                                                    |
| RemoteEstimateID             | This field displays the estimate id passed in during the creation of the given repair order by a remote application.                                                                                  |
| ROAge                        | This field displays the age (current date - open date) of the given repair order.                                                                                                                     |
| ROArrivalDateTime            | This field displays the date on which the unit first arrived for service.                                                                                                                             |
| ROBillingHours               | This field displays the number of hours that the customer will be billed for on the given repair order.                                                                                               |
| ROBookHours                  | This field displays the amount of time that the given repair order was estimated to take.                                                                                                             |
| IsROClockedON                | This field displays whether any technicians are currently clocked on to the given repair order.                                                                                                       |
| ROClockedONTechnicians       | This field displays the technicians that are currently clocked onto the given repair order.                                                                                                           |
| IsROCompleted                | This field displays whether the given repair order has been completed.                                                                                                                                |
| RO Customer PO Number        | This field displays the customer purchase order number for the customer associated with the given repair order.                                                                                       |
| RODateCompleted              | This field displays the date on which the given repair order was completed.                                                                                                                           |
| RODateInvoiced               | This field displays the date on which the given repair order was invoiced.                                                                                                                            |
| RODateOpened                 | This field displays the date on which the given repair order was opened.                                                                                                                              |
| RODaysCompletedToInvoiced    | This field displays the number of days that passed between the date the repair order was completed and the date it was invoiced.                                                                      |
| RODaysSinceLastWorkedOn      | This field displays the number of days that have passed since the repair order was last worked on.                                                                                                    |
| ROEHCCharges                 | This field displays the total amount charged to the customer for EHC charges on the given repair order.                                                                                               |
| ROHoursBilled                | This field displays the total hours billed on the given repair order.                                                                                                                                 |
| ROHoursSinceLastWorkedOn     | This field displays the number of hours that have passed since the repair order was last worked on.                                                                                                   |
| ROHoursWorked                | This field displays the total number of hours that have been worked on the given repair order.                                                                                                        |
| ROLaborCharges               | This field displays the total amount charged to the customer for labor on the given repair order.                                                                                                     |
| ROLaborCost                  | This field displays the total cost of the labor on the given repair order.                                                                                                                            |
| ROMiscellaneousCharges       | This field displays the total amount charged to the customer for miscellaneous charges on the given repair order.                                                                                     |
| ROMiscellaneousChargesCost   | This field displays the total cost of the miscellaneous charges on the given repair order.                                                                                                            |
| RONumber                     | This field displays the repair order number identifying the given repair order.                                                                                                                       |
| ROOpenTime                   | This field displays the amount of time that the technicians currently clocked in to the given repair order have been clocked in.                                                                      |
| ROPartsAverageCost           | This field displays the total average cost of the parts on the given repair order.                                                                                                                    |
| ROPartsCharges               | This field displays the total amount charged to the customer for parts on the given repair order.                                                                                                     |
| ROPartsReplacementCost       | This field displays the total cost of the parts, based on replacement cost, on the given repair order.                                                                                                |
| ROPartsSellingCost           | This field displays the total selling cost of the parts on the given repair order.                                                                                                                    |
| ROPerformance                | This field displays the difference between the hours billed and the hours worked on the given repair order.                                                                                           |
| ROPromiseDateTime            | This field displays the date on which the given repair order was promised to be completed.                                                                                                            |
| ROPromisedDays               | This field displays the days left until the given repair order should be completed (promised date - current date).                                                                                    |
| ROPromisedHours              | This field displays the hours left until the given repair order should be completed (promised date - current date).                                                                                   |
| RORemainingHours             | This field displays the number of hours left between the total number of hours that have been worked and the number of hours that were originally billed on the given repair order.                   |
| ROStatus                     | This field displays the status of the given repair order.                                                                                                                                             |
| ROTaskCount                  | This field displays the number of tasks that are associated with the given repair order.                                                                                                              |
| ROTechnicians                | This field displays the technicians that have been added to the given repair order.                                                                                                                   |
| ROTotalAverageCost           | This field displays the total cost of all charges on the given repair order (average cost for parts).                                                                                                 |
| RO Total Replacement Cost    | This field displays the total cost of all charges on the given repair order (replacement cost for parts).                                                                                             |
| ROTotalSellingCost           | This field displays the total cost of all charges on the given repair order (selling cost for parts).                                                                                                 |
| IsROWaiting                  | This field displays whether the given repair order is waiting on any tasks to be completed.                                                                                                           |
| IsROWaitingForParts          | This field displays whether the given repair order is waiting on any backordered parts to arrive.                                                                                                     |
| ROWaitingTasksCount          | This field displays the number of tasks on the given repair order that are currently waiting for either parts or labor.                                                                               |
| SalesTaxSetting              | This field displays whether sales tax will be applied to the given repair order based on the local tax body or the tax body associated with the billing customer.                                     |
| SalesTaxTotal                | This field displays the total sales tax on the given repair order.                                                                                                                                    |
| Salesperson                  | This field displays the salesperson associated with the given repair order, from the billing customer tab in the repair order application.                                                            |
| TaxBody                      | This field displays the tax body associated with the given repair order.                                                                                                                              |
| TaxStatus                    | This field displays the tax status associated with the given repair order.                                                                                                                            |
| TotalROCharges               | This field displays the total amount charged to the customer on the given repair order.                                                                                                               |
| UnitMake                     | This field displays the make of the unit on the given repair order.                                                                                                                                   |
| UnitMeterReading             | This field displays the meter reading recorded for the unit at the time of the given repair order.                                                                                                    |
| UnitModel                    | This field displays the model of the unit on the given repair order.                                                                                                                                  |
| UnitYear                     | This field displays the year of the unit on the given repair order.                                                                                                                                   |
| VIN                          | This field displays the Vehicle Identification Number associated with the unit on the given repair order.                                                                                             |
| IsVoided                     | This field displays whether the given repair order has been voided.                                                                                                                                   |
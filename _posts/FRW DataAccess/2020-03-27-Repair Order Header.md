---
layout: post
title: "Repair Order Header"
category: "Repair Order"
icon: "icon-wrench"
type: "data_access" 
comments: false
description: Access all information about Open and Invoiced Repair Orders.  This includes the header, task, part, labor, and miscellaneous charge detail items on a given repair order
---
 
---
---
This data object is used to display the header records for all repair orders in Fusion, and contains one record for each order with summary information about the repair order included. This data object can be joined to Repair Order Task and then to Repair Order Details in order to view the detail information on the repair order.

This information can be found in the repair order application in Fusion.

#### URL
```
/frw/RepairOrderHeader
```

<hr>
Field Details...

| **SQL Field Name**           | **Column Description**               |  **Fusion Version (or later)**
|---|---|---|
| AddDate                      | This field displays the date on which the given repair order was added to the system.                                                                                                                 | |
| ROServiceWriter              | This field displays, if available, the username of the user who created the given repair order or the username of the user who invoiced the given repair order.                                       | |
| AuthorizationNumber          | This field displays the credit authorization number associated with the given repair order, from the billing customer tab in the repair order application.                                            | |
| BillingContactname           | This field displays the name of the contact associated with the billing customer associated with the given repair order.                                                                              | |
| BillingCustomerAccountStatus | This field displays the current status of the customer account for the billing customer associated with the given repair order.                                                                       | |
| BillingCustomerAddress       | This field displays the street address of the billing customer associated with the given repair order.                                                                                                | |
| BillingCustomerCity          | This field displays the city of the billing customer associated with the given repair order.                                                                                                          | |
| BillingCustomerCountry       | This field displays the country of the billing customer associated with the given repair order.                                                                                                       | |
| BillingCustomerCounty        | This field displays the county of the billing customer associated with the given repair order.                                                                                                        | |
| BillingCustomerIndustryType  | This field displays the industry type of the billing customer associated with the given repair order.                                                                                                 | |
| BillingCustomerName          | This field displays the company name of the billing customer associated with the given repair order.                                                                                                  | |
| BillingCustomerNumber        | This field displays the customer number of the billing customer associated with the given repair order.                                                                                               | |
| BillingCustomerPostalCode    | This field displays the postal code of the billing customer associated with the given repair order.                                                                                                   | |
| BillingCustomerRegion        | This field displays the region of the billing customer associated with the given repair order.                                                                                                        | |
| IsBillingCustomerWarranty    | This field displays whether the billing customer associated with the given repair order is a warranty customer.                                                                                       | |
| BillingCustomerWorkPhone     | This field displays the work phone number for the billing customer associated with the given repair order.                                                                                            | |
| BillingHomePhone             | This field displays the home phone number of the contact associated with the billing customer associated with the given repair order.                                                                 | |
| Branch                       | This field displays the branch in which the given repair order was created.                                                                                                                           | |
| CharacteristicType           | This field displays the characteristic type of the unit on the given repair order.                                                                                                                    | |
| CompletedToInvoicedInterval  | This field displays the category the given repair order falls into based on the number of days that passed between completion and invoicing (00-01, 02-05, 06-10, 11-20, 21-30, 31-45, and 45+ days). | |
| ContactHomePhone             | This field displays the home phone number of the contact associated with the unit owning customer associated with the given repair order.                                                             | |
| ContactName                  | This field displays the name of the contact associated with the unit owning customer associated with the given repair order.                                                                          | |
| ContactWorkPhone             | This field displays the work phone number of the contact associated with the unit owning customer associated with the given repair order.                                                             | |
| CreditReserve                | This field displays the credit reserve amount associated with the given repair order.                                                                                                                 | |
| CustomerAccountStatus        | This field displays the current status of the customer account for the unit owning customer associated with the given repair order.                                                                   | |
| CustomerAddress              | This field displays the street address of the unit owning customer associated with the given repair order.                                                                                            | |
| CustomerBaseBranch           | This field displays the base branch that the unit owning customer on the given repair order is associated with.                                                                                       | |
| CustomerCity                 | This field displays the city of the unit owning customer associated with the given repair order.                                                                                                      | |
| CustomerName                 | This field displays the company name of the unit owning customer associated with the given repair order.                                                                                              | |
| CustomerNumber               | This field displays the customer number of the unit owning customer associated with the given repair order.                                                                                           | |
| CustomerPhone                | This field displays the phone number for the unit owning customer associated with the given repair order.                                                                                             | |
| CustomerPostalCode           | This field displays the postal code of the unit owning customer associated with the given repair order.                                                                                               | |
| CustomerRegion               | This field displays the region of the unit owning customer associated with the given repair order.                                                                                                    | |
| CustomerUnitNumber           | This field displays the unit number associated with the given repair order, owned by the unit owning customer.                                                                                        | |
| IsCustomerWarranty           | This field displays whether the unit owning customer associated with the given repair order is a warranty customer.                                                                                   | |
| DaysArrivalToFirstPunch      | This field displays the number of days between the arrival date on the repair order and the first time punch in on the repair order.                                                                  | |
| DaysFirstPunchToLastPunch    | This field displays the number of days between the first time punch in and the last time punch out on the repair order.                                                                               | |
| DaysOpenToFirstPunch         | This field displays the number of days between the open date on the repair order and the first time punch in on the repair order.                                                                     | |
| Department                   | This field displays the department in which the given repair order was created.                                                                                                                       | |
| Division                     | This field displays the division in which the given repair order was created.                                                                                                                         | |
| ECMReading                   | This field displays the ECM meter reading recorded for the unit at the time of the given repair order.                                                                                                | |
| EmailAddressOfCustomer       | This field displays the email address provided for the customer on the given repair order.                                                                                                            | |
| FirstPunchDate               | This field displays the first time punch in on the repair order.                                                                                                                                      | |
| FollowUpEmailFlag            | This field displays whether the given repair order requires a follow up email.                                                                                                                        | |
| InServiceDate                | This field displays the date on which the given unit first went into service.                                                                                                                         | |
| IndustryType                 | This field displays the industry type of the unit owning customer associated with the given repair order.                                                                                             | |
| InvoiceDueDate               | This field displays the date on which the given repair order invoice is due to be paid.                                                                                                               | |
| InvoiceNumber                | This field displays the invoice number of the given invoiced repair order.                                                                                                                            | |
| InvoiceUser                  | This field displays the username of the user who invoiced the given repair order.                                                                                                                     | |
| LastPunchDate                | This field displays the last time punch out on the repair order.                                                                                                                                      | |
| LastUpdate                   | This field displays the date on which the given repair order was last updated in the system.                                                                                                          | |
| UpdateUser                   | This field displays the username of the user who last updated the given repair order.                                                                                                                 | |
| LPONumber                    | This field displays the local purchase order number associated with the given repair order.                                                                                                           | |
| MeterType                    | This field displays the unit of measure associated with the meter reading for the unit on the given repair order.                                                                                     | |
| OriginalRONumber             | This field displays the repair order number from the original repair order for repair orders that were created from another repair order, as a spinoff.                                               | |
| PaymentMethod                | This field displays the method by which the repair order will be paid by the billing customer.                                                                                                        | |
| RemoteApplication            | This field displays the name of the remote application that the given repair order was created by.                                                                                                    | |
| RemoteEstimateID             | This field displays the estimate id passed in during the creation of the given repair order by a remote application.                                                                                  | |
| ROAge                        | This field displays the age (current date - open date) of the given repair order.                                                                                                                     | |
| ROArrivalDateTime            | This field displays the date on which the unit first arrived for service.                                                                                                                             | |
| ROBillingHours               | This field displays the number of hours that the customer will be billed for on the given repair order.                                                                                               | |
| ROBookHours                  | This field displays the amount of time that the given repair order was estimated to take.                                                                                                             | |
| IsROClockedON                | This field displays whether any technicians are currently clocked on to the given repair order.                                                                                                       | |
| ROClockedONTechnicians       | This field displays the technicians that are currently clocked onto the given repair order.                                                                                                           | |
| IsROCompleted                | This field displays whether the given repair order has been completed.                                                                                                                                | |
| RO Customer PO Number        | This field displays the customer purchase order number for the customer associated with the given repair order.                                                                                       | |
| RODateCompleted              | This field displays the date on which the given repair order was completed.                                                                                                                           | |
| RODateInvoiced               | This field displays the date on which the given repair order was invoiced.                                                                                                                            | |
| RODateOpened                 | This field displays the date on which the given repair order was opened.                                                                                                                              | |
| RODaysCompletedToInvoiced    | This field displays the number of days that passed between the date the repair order was completed and the date it was invoiced.                                                                      | |
| RODaysSinceLastWorkedOn      | This field displays the number of days that have passed since the repair order was last worked on.                                                                                                    | |
| ROEHCCharges                 | This field displays the total amount charged to the customer for EHC charges on the given repair order.                                                                                               | |
| ROHoursBilled                | This field displays the total hours billed on the given repair order.                                                                                                                                 | |
| ROHoursSinceLastWorkedOn     | This field displays the number of hours that have passed since the repair order was last worked on.                                                                                                   | |
| ROHoursWorked                | This field displays the total number of hours that have been worked on the given repair order.                                                                                                        | |
| ROLaborCharges               | This field displays the total amount charged to the customer for labor on the given repair order.                                                                                                     | |
| ROLaborCost                  | This field displays the total cost of the labor on the given repair order.                                                                                                                            | |
| ROMiscellaneousCharges       | This field displays the total amount charged to the customer for miscellaneous charges on the given repair order.                                                                                     | |
| ROMiscellaneousChargesCost   | This field displays the total cost of the miscellaneous charges on the given repair order.                                                                                                            | |
| RONumber                     | This field displays the repair order number identifying the given repair order.                                                                                                                       | |
| ROOpenTime                   | This field displays the amount of time that the technicians currently clocked in to the given repair order have been clocked in.                                                                      | |
| ROPartsAverageCost           | This field displays the total average cost of the parts on the given repair order.                                                                                                                    | |
| ROPartsCharges               | This field displays the total amount charged to the customer for parts on the given repair order.                                                                                                     | |
| ROPartsReplacementCost       | This field displays the total cost of the parts, based on replacement cost, on the given repair order.                                                                                                | |
| ROPartsSellingCost           | This field displays the total selling cost of the parts on the given repair order.                                                                                                                    | |
| ROPerformance                | This field displays the difference between the hours billed and the hours worked on the given repair order.                                                                                           | |
| ROPromiseDateTime            | This field displays the date on which the given repair order was promised to be completed.                                                                                                            | |
| ROPromisedDays               | This field displays the days left until the given repair order should be completed (promised date - current date).                                                                                    | |
| ROPromisedHours              | This field displays the hours left until the given repair order should be completed (promised date - current date).                                                                                   | |
| RORemainingHours             | This field displays the number of hours left between the total number of hours that have been worked and the number of hours that were originally billed on the given repair order.                   | |
| ROStatus                     | This field displays the status of the given repair order.                                                                                                                                             | |
| ROTaskCount                  | This field displays the number of tasks that are associated with the given repair order.                                                                                                              | |
| ROTechnicians                | This field displays the technicians that have been added to the given repair order.                                                                                                                   | |
| ROTotalAverageCost           | This field displays the total cost of all charges on the given repair order (average cost for parts).                                                                                                 | |
| RO Total Replacement Cost    | This field displays the total cost of all charges on the given repair order (replacement cost for parts).                                                                                             | |
| ROTotalSellingCost           | This field displays the total cost of all charges on the given repair order (selling cost for parts).                                                                                                 | |
| IsROWaiting                  | This field displays whether the given repair order is waiting on any tasks to be completed.                                                                                                           | |
| IsROWaitingForParts          | This field displays whether the given repair order is waiting on any backordered parts to arrive.                                                                                                     | |
| ROWaitingTasksCount          | This field displays the number of tasks on the given repair order that are currently waiting for either parts or labor.                                                                               | |
| SalesTaxSetting              | This field displays whether sales tax will be applied to the given repair order based on the local tax body or the tax body associated with the billing customer.                                     | |
| SalesTaxTotal                | This field displays the total sales tax on the given repair order.                                                                                                                                    | |
| Salesperson                  | This field displays the salesperson associated with the given repair order, from the billing customer tab in the repair order application.                                                            | |
| TaxBody                      | This field displays the tax body associated with the given repair order.                                                                                                                              | |
| TaxStatus                    | This field displays the tax status associated with the given repair order.                                                                                                                            | |
| TotalROCharges               | This field displays the total amount charged to the customer on the given repair order.                                                                                                               | |
| UnitMake                     | This field displays the make of the unit on the given repair order.                                                                                                                                   | |
| UnitMeterReading             | This field displays the meter reading recorded for the unit at the time of the given repair order.                                                                                                    | |
| UnitModel                    | This field displays the model of the unit on the given repair order.                                                                                                                                  | |
| UnitYear                     | This field displays the year of the unit on the given repair order.                                                                                                                                   | |
| VIN                          | This field displays the Vehicle Identification Number associated with the unit on the given repair order.                                                                                             | |
| IsVoided                     | This field displays whether the given repair order has been voided.                                                                                                                                   | |
| AssessmentCompletedUser      |  This field will display the username of the person who completed the assessment.| TBD |
| AssessmentCompletedDate      |  This field will display the date and time that the assessment of the unit was completed.| TBD|
| CustomerContactedUser        |  This field will display the username of the person who contacted the customer.   | TBD|
| CustomerContactedDate        |  This field will display the date and time that the customer was contacted for the repair order.                  | TBD |
| CustomerServiceBeginDate     |  This field will display the date and time that the customer requested that the service work begin for the unit.| TBD|
| DealerServiceBeginDate       |  This field will display the date and time that the dealer scheduled for the work to begin for the unit.| TBD|
| RepairTypeCode               |  This field will display the Repair Type Code that was used for the Allison Transmission Integration.| TBD |
| ROEstimatedAmount            |  This field will display the total RO Estimated Amount -  This field is used by the Wheeltime integration and can be updated from Decisiv. | TBD|
| SendROUpdates                |  This field will display whether or not the customer is being sent RO updates when the RO status changes for the Wheeltime integration.| TBD|

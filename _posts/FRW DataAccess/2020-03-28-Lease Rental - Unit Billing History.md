---
layout: post
title: "Lease Rental Unit Billing History"
category: "Lease / Rental" 
icon: "icon-user-plus1"
type: "data_access" 
comments: false
description: Access the lease rental billing history information for each unit on a given LR invoice from the Fusion business system
---

---
---
This data object is used to return the lease rental billing history information for each unit on a given LR invoice from the Fusion business system.

This is found within the Lease Rental Billing History program in the Fusion business system.

 
#### URL 
```
/frw/LRBillingHistory
``` 
 <hr>
Field Details...

| **SQL Field Name**         | **Column Description**                                                                                                                                                          |
|---|---|
| AddDate                    | This field displays the date on which the given LR invoice was added to the system.                                                                                             |
| AddUser                    | This field displays the user name of the user who added the given LR invoice.                                                                                                   |
| Branch                     | This field displays the branch in which the given LR invoice was created.                                                                                                       |
| CompanyName                | This field displays the company name of the customer associated with the given LR invoice.                                                                                      |
| ContractNumber             | This field displays the contract number of the given invoiced LR contract.                                                                                                      |
| ContractSalesperson        | This field displays the salesperson listed on the given LR contract.                                                                                                            |
| CustomerKey                | This field displays the identifying number of the customer associated with the given LR invoice.                                                                                |
| Department                 | This field displays the department in which the given LR invoice was created.                                                                                                   |
| Division                   | This field displays the division in which the given LR invoice was created.                                                                                                     |
| FixedChargeBillingGroup    | This field displays the billing group used for the fixed charges on the given LR invoice.                                                                                       |
| FixedChargeEndDate         | This field displays the end of the period for which billing on fixed charges was calculated for the given LR invoice.                                                           |
| FixedChargeStartDate       | This field displays the beginning of the period for which billing on fixed charges was calculated for the given LR invoice.                                                     |
| InvoiceDate                | This field displays the date on which the given LR invoice was invoiced.                                                                                                        |
| InvoiceNumber              | This field displays the invoice number of the given LR invoice.                                                                                                                 |
| LastUpdateDate             | This field displays the date on which the given LR invoice was last updated.                                                                                                    |
| LastUpdateUser             | This field displays the user name of the user who last updated the given LR invoice.                                                                                            |
| Make                       | This field displays the make of the given unit on the LR invoice.                                                                                                               |
| MeterAtBilling             | This field displays the current meter reading of the given unit at the time the given LR invoice was billed.                                                                    |
| Model                      | This field displays the model of the given unit on the LR invoice.                                                                                                              |
| PostingPeriod              | This field displays the period in which the given LR invoice was posted.                                                                                                        |
| PreviouslyBilledMeter      | This field displays the meter reading of the given unit the last time it was billed on an LR invoice or, if no previous billings exist, the starting meter reading of the unit. |
| UnitFixedChargeTotal       | This field displays the total amount of the fixed charges associated with the given unit on the LR invoice.                                                                     |
| UnitMiscChargeTotal        | This field displays the total amount of the miscellaneous charges associated with the given unit on the LR invoice.                                                             |
| UnitNumber                 | This field displays the unit number of the given unit on the invoiced LR contract.                                                                                              |
| UnitSalesperson            | This field displays the salesperson listed with the given unit on the given LR contract.                                                                                        |
| UnitTotal                  | This field displays the total amount of the charges associated with the given unit on the LR invoice.                                                                           |
| UnitVariableChargeTotal    | This field displays the total amount of the variable charges associated with the given unit on the LR invoice.                                                                  |
| VariableChargeBillingGroup | This field displays the billing group used for the variable charges on the given LR invoice.                                                                                    |
| VariableChargeEndDate      | This field displays the end of the period for which billing on variable charges was calculated for the given LR invoice.                                                        |
| VariableChargeStartDate    | This field displays the beginning of the period for which billing on variable charges was calculated for the given LR invoice.                                                  |
| VIN                        | This field displays the vehicle identification number of the given unit on the LR invoice.                                                                                      |
| IsVoided                   | This field displays whether the given LR invoice has been voided.                                                                                                               |
| Year                       | This field displays the year of the given unit on the LR invoice.                                                                                                               | 

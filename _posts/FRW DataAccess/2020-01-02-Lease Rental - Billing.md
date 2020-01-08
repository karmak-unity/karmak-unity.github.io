---
layout: post
title: "Lease - Rental Billing"
category: "Lease / Rental" 
icon: "icon-user-plus1"
type: "data_access" comments: falsedescription: Access all billing information, history, and details related to lease rentals
---

---
---
### Lease Rental Billing Group
---

This data object is used to display the name and billing information for each of
the lease rental billing groups in the Fusion business system.

This information is found in the Lease Rental Billing Group application in the
Fusion business system.

 <!-- SQL VIEW:  **vwLR_SSR_LRBillingGroup**



 -->  <hr>Field Details...

| **SQL Field Name**    | **Column Description**                                                                              |
|---|---|
| AddDate               | This field displays the date on which the given LR billing group was added to the system.           |
| AddUser               | This field displays the user name of the user who added the given LR billing group.                 |
| BillingCycleFrequency | This field displays the frequency at which the given LR billing group is billed.                    |
| BillingCycleType      | This field displays the type of billing that is applied to the given LR billing group.              |
| LastBilledDate        | This field displays the date on which the the last billing for the given LR billing group occurred. |
| LastUpdateDate        | This field displays the date on which the given LR billing group was last updated.                  |
| UpdateUser            | This field displays the user name of the user who last updated the given LR billing group.          |
| NAME                  | This field displays the name of the given LR billing group.                                         |

---
---

### Lease Rental Unit Billing History
---

This data object is used to return the lease rental billing history information
for each unit on a given LR invoice from the Fusion business system.

This is found within the Lease Rental Billing History program in the Fusion
business system.

 <!-- SQL VIEW:  **vwLR_SSR_LRBillingHistory**



 -->  <hr>Field Details...

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

---
---

### Lease Rental Billing History Detail
---

This data object is used to return the detail for all charges associated with a
given unit on an LR invoice from the Fusion business system.

This is found within the Lease Rental Billing History program in the Fusion
business system.

 <!-- SQL VIEW:  **vwLR_SSR_LRBillingHistoryDetail**



 -->  <hr>Field Details...

| **SQL Field Name**   | **Column Description**                                                                                       |
|---|---|
| AddDate              | This field displays the date on which the given LR invoice was added to the system.                          |
| AddUser              | This field displays the user name of the user who added the given LR invoice to the system.                  |
| BillingRateFrequency | This field displays the frequency at which the given fixed charge on the LR invoice is billed.               |
| Branch               | This field displays the branch in which the given LR invoice was created.                                    |
| Charge               | This field displays the name of the given charge on the LR invoice.                                          |
| ChargeDescription    | This field displays the description of the given charge on the LR invoice.                                   |
| ChargeType           | This field displays the type of the given charge on the LR invoice, Fixed, Variable, Miscellaneous, or Fuel. |
| CompanyName          | This field displays the company name of the customer associated with the given LR invoice.                   |
| ContractNumber       | This field displays the contract number of the LR contract on the given LR invoice.                          |
| ContractSalesperson  | This field displays the salesperson listed on the given LR contract.                                         |
| Cost                 | This field displays the cost of the given charge on the LR invoice.                                          |
| CustomerKey          | This field displays the identifying number of the customer associated with the given LR invoice.             |
| Department           | This field displays the department in which the given LR invoice was created.                                |
| Division             | This field displays the division in which the given LR invoice was created.                                  |
| ExtendedCost         | This field displays the extended cost (cost \* quantity) of the given charge on the LR invoice.              |
| ExtendedRate         | This field displays the extended rate (rate \* quantity) of the given charge on the LR invoice.              |
| InvoiceDate          | This field displays the date on which the given LR invoice was invoiced.                                     |
| InvoiceNumber        | This field displays the invoice number of the given LR invoice.                                              |
| LastUpdateDate       | This field displays the date on which the given LR invoice was last updated in the system.                   |
| LastUpdateUser       | This field displays the user name of the user who last updated the given LR invoice in the system.           |
| MeterType            | This field displays the meter type of the given variable charge on the LR invoice.                           |
| Quantity             | This field displays the quantity of the given charge on the LR invoice.                                      |
| Rate                 | This field displays the rate charged to the customer for the given charge on the LR invoice.                 |
| Status               | This field displays the status of the given LR invoice as invoiced or voided.                                |
| StockNumber          | This field displays the stock number of the unit on the given LR invoice.                                    |
| UnitNumber           | This field displays the unit number of the unit on the given LR invoice.                                     |
| UnitSalesperson      | This field displays the salesperson listed with the given unit on the given LR contract.                     |
| UnitStatus           | This field displays the status of the unit at the time of the given LR invoice.                              |
| IsVoided             | This field displays whether the given LR invoice has been voided.                                            |

---
---
### Lease Rental Billing History
---

This data object is used to display the overall totals and information about a
given LR invoice.

This information can be found in the LR Billing History application in the
Fusion business system.

 <!-- SQL VIEW:  **vwLR_SSR_LRBillingHistoryHeader**



 -->  <hr>Field Details...

| **SQL Field Name**   | **Column Description**                                                                                           |
|---|---|
| AddDate              | This field displays the date on which the given LR invoice was added to the system.                              |
| AddUser              | This field displays the user name of the user who added the given LR invoice to the system.                      |
| Branch               | This field displays the branch in which the given LR invoice was created.                                        |
| CompanyName          | This field displays the company name of the customer associated with the given LR invoice.                       |
| ContractNumber       | This field displays the contract number of the LR contract on the given LR invoice.                              |
| ContractSalesperson  | This field displays the salesperson listed on the given LR contract.                                             |
| CustomerKey          | This field displays the identifying number of the customer associated with the given LR invoice.                 |
| Department           | This field displays the department in which the given LR invoice was created.                                    |
| Division             | This field displays the division in which the given LR invoice was created.                                      |
| DueDate              | This field displays the date on which the given LR invoice is due to be paid.                                    |
| FixedBillingGroup    | This field displays the billing group used for the fixed charges on the given LR invoice.                        |
| InvoiceDate          | This field displays the date on which the given LR invoice was invoiced.                                         |
| InvoiceNumber        | This field displays the invoice number of the given LR invoice.                                                  |
| LastUpdateDate       | This field displays the date on which the given LR invoice was last updated in the system.                       |
| LastUpdateUser       | This field displays the user name of the user who last updated the given LR invoice in the system.               |
| PaymentMethod        | This field displays the payment method by which the customer will be paying the given LR invoice.                |
| PaymentTerms         | This field displays the payment terms which apply to the customer regarding the payment of the given LR invoice. |
| PostingPeriod        | This field displays the period in which the given LR invoice was posted.                                         |
| Subtotal             | This field displays the total amount of the fixed, variable, and miscellaneous charges on the given LR invoice.  |
| TotalFixed           | This field displays the total amount of the fixed charges on the given LR invoice.                               |
| TotalInvoice         | This field displays the total amount of the given LR invoice, including all charges and taxes.                   |
| TotalMisc            | This field displays the total amount of the miscellaneous charges on the given LR invoice.                       |
| TotalTax             | This field displays the total amount of taxes charged on the given LR invoice.                                   |
| TotalVariable        | This field displays the total amount of the variable charges on the given LR invoice.                            |
| VariableBillingGroup | This field displays the billing group used for the variable charges on the given LR invoice.                     |
| IsVoided             | This field displays whether the given LR invoice has been voided.                                                |


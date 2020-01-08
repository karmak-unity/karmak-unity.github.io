---
layout: post
title: "Lease - Rental Charges and Contracts"
category: "Lease / Rental" 
icon: "icon-user-plus1"
type: "data_access" comments: falsedescription: Access all customer insurance information from the Fusion business system
---

---
---
### Lease Rental Charges
---

This data object is used to return lease rental charge information from the
Fusion business system.

This information is pulled from the Lease Rental Miscellaneous, Fixed, and
Variable Charge programs within the Fusion business system.

 <!-- SQL VIEW:  **vwLR_SSR_LRCharges**



 -->  <hr>Field Details...

| **SQL Field Name**    | **Column Description**                                                                                            |
|---|---|
| AddDate               | This field will display the date and time the record was added to the system.                                     |
| AddUser               | This field displays the user name that added the record.                                                          |
| BillingFrequency      | This field displays how often billing is completed.                                                               |
| Charge                | This field displays the name of the LR Charge.                                                                    |
| ChargeType            | This field displays the type of charge observed.                                                                  |
| Lease                 | This field displays a charge for a lease contract.                                                                |
| Maintenance           | This field displays a charge for a maintenance contract.                                                          |
| Rental                | This field displays a charge for a rental contract.                                                               |
| CostRequired          | This field displays whether or not a user will be required  to input a cost when adding the charge to a contract. |
| DescOverride          | This field displays whether or not a user can override the description of charge when adding it to a contract.    |
| Inactive              | This field displays whether or not a given charge is set to inactive.                                             |
| InvoiceDescription    | This field displays the description of a given invoice, based on the invoicing module.                            |
| LastUpdateDate        | This field will display the date and time the record was last updated.                                            |
| UpdateUser            | This field displays the user name of the individual who made the last update.                                     |
| LeaseRentalChargeType | This field displays the type of charge on a contract.                                                             |
| MeterType             | This field displays the unit's meter type (gallons, hours, kilometers, etc.).                                     |
| ProductClass          | This field displays the product class associated with a given charge.                                             |
| TaxCode               | This field displays the tax code assigned to a customer.                                                          |
| TaxStatusOverride     | This field displays which tax status the charge should look at when determining the tax.                          |

---
---
### Lease Rental Contract
---

This data object is used to return all information from the Lease Rental
Contract program from within the Fusion business system.

This is found within the Lease Rental Contract program within the Fusion
business system.

 <!-- SQL VIEW:  **vwLR_SSR_LRContract**



 -->  <hr>Field Details...

| **SQL Field Name**         | **Column Description**                                                                              |
|---|---|
| AddDate                    | This field displays the date on which the contract was added.                                       |
| AddUser                    | This field displays the user name that added the record.                                            |
| Address1                   | This field displays address line one of the address on the contract.                                |
| Address2                   | This field displays address line two of the address on the contract.                                |
| BranchCode                 | This field displays branch associated with the LR Contract.                                         |
| City                       | This field displays the city entered on the LR Contract.                                            |
| CompanyName                | This field displays the company name of the customer associated with the LR contract.               |
| ContractNumber             | This field displays the number attached to a contract.                                              |
| LeaseContractStatus        | This field displays the status of a given contract.                                                 |
| ContractType               | This field displays the type of a given contract (Lease, Rental, Maintenance).                      |
| Country                    | This field displays the customer's country.                                                         |
| County                     | This field displays the customer's county.                                                          |
| CustomerKey                | This field displays the identifying number attached to a customer.                                  |
| CustomerPO                 | This field displays the customer purchase order associated with an invoiced sale.                   |
| CVOR                       | This field displays the Commercial Vehicle Operator's Registration.                                 |
| Department                 | This field displays the department associated with a LR Contract.                                   |
| DOT                        | This field displays the Department of Transportation ID number.                                     |
| EMail                      | This field displays the customer's email address from the address entry tab.                        |
| Fax                        | This field displays the customer's fax number from the address entry tab.                           |
| FixedChargeBillingGroup    | This field displays the billing group used for fixed charges.                                       |
| LastUpdateDate             | This field displays the last date the record was updated.                                           |
| UpdateUser                 | This field displays the user name of the individual who made the update.                            |
| UserDefinedPaymentMethod   | This field displays the payment method for a customer, as defined by the user.                      |
| Phone                      | This field displays the customer's primary phone number from the address entry tab.                 |
| Phone2                     | This field displays the customer's secondary phone number from the address entry tab on a contract. |
| Phone3                     | This field displays the customer's tertiary phone number from the address entry tab on a contract.  |
| PostalCode                 | This field displays the customer's postal code.                                                     |
| Region                     | This field displays the customer's region or state.                                                 |
| SalesTaxSetting            | This field displays whether the tax body is defaulted to local or customer's tax body.              |
| UserName                   | This field displays the salesperson associated with a lease and rental contract.                    |
| SubsAllowed                | This field displays whether the units on the given lease contract are able to substituted.          |
| TaxBody                    | This field displays the tax body associated with a customer address.                                |
| TaxStatus                  | This field displays the customer's tax status on a contract (taxable, exempt, etc.).                |
| VariableChargeBillingGroup | This field displays the billing used for variable charges.                                          |
| WebAddress                 | This field displays the customer's web address  from the address entry tab on a contract.           |

---
---
### Lease Rental Contract Unit
---

This data object is used to return all information from a unit on a lease or
rental contract from within the Fusion business system.

This is found within the Lease Rental Contract Unit program within the Fusion
business system.

 <!-- SQL VIEW:  **vwLR_SSR_LRContractUnit**



 -->  <hr>Field Details...

| **SQL Field Name**                     | **Column Description**                                                                                                                        |
|---|---|
| AddDate                                | This field display the date and time the record was added.                                                                                    |
| AddUser                                | This field displays the user name that added the record.                                                                                      |
| AllowedForFixed                        | This field displays what percentage of the new CPI a customer is subject to for fixed charges.                                                |
| AllowedForVariable                     | This field displays what percentage of the new CPI a customer is subject to for variable charges.                                             |
| Area                                   | This field displays the location where commodities are being hauled.                                                                          |
| BillFuelTicketOnLRInvoice              | This field displays whether or not the unit will have fuel invoices charged to it.                                                            |
| CharacteristicType                     | This field displays the unit's characteristic type (truck, trailer, reefer, etc.).                                                            |
| ChildUnits                             | This field displays whether or not the given unit has any child units attached to it.                                                         |
| ChildUnitsOnContract                   | This field displays whether or not the given unit has any child units  added on the contract.                                                 |
| Commodity                              | This field displays the commodity that will be hauled in then given vehicle.                                                                  |
| ContractNumber                         | This field displays the number attached to a contract.                                                                                        |
| LeaseContractStatus                    | This field displays the status of the  given contract.                                                                                        |
| CustomerPO                             | This field displays the customer purchase order associated with the given unit.                                                               |
| FirstName                              | This field displays the driver's first name.                                                                                                  |
| LastName                               | This field displays the driver's last name.                                                                                                   |
| DriverMiddleInitial                    | This field displays the driver's middle initial.                                                                                              |
| EndingMeter                            | This field displays the meter reading for the given unit when the contract ended.                                                             |
| EquipmentClass                         | This field displays the classification of inventory, such as different size trailers.                                                         |
| EquipmentType                          | This field displays the equipment type of the given unit.                                                                                     |
| EstimatedBilledMeter                   | This field displays the value used to calculate the variable billing for each billing cycle.                                                  |
| FleetType                              | This field displays the fleet type for the given unit.                                                                                        |
| IsHazardous                            | This field displays whether or not a commodity being hauled is hazardous.                                                                     |
| LastBillThruFixed                      | This field displays the date the unit is billed thru for fixed charges.                                                                       |
| LastBillThruVariable                   | This field displays the date the unit is billed thru for variable charges.                                                                    |
| LastCPI                                | This field displays the Consumer Price Index number when CPI was last calculated.                                                             |
| LastUpdateDate                         | This field display the date and time the record was last updated.                                                                             |
| UpdateUser                             | This field displays the user name of the individual who made the update.                                                                      |
| ExpirationDate                         | This field displays the date on which a customer's liability insurance policy expires.                                                        |
| PolicyNumber                           | This field displays the customer's liability insurance policy number.                                                                         |
| InsuranceProvider                      | This field displays the name of a customer's liability insurance provider.                                                                    |
| LicenseExpiration                      | This field displays the date on which a driver's license expires.                                                                             |
| LicenseNumber                          | This field displays the driver's license number of the driver on a unit.                                                                      |
| RentalRate                             | This field displays the rental rate for a reservation or agreement.                                                                           |
| Make                                   | This field displays the make of the given unit.                                                                                               |
| MaxAnnualMeter                         | This field displays the maximum annual meter reading on the given unit.                                                                       |
| MaxAnnualofIncreaseFixed               | This field displays the maximum annual adjustment allowable increase for Fixed Charges, based on the increase in the Consumer Price Index.    |
| MaxAnnualofIncreaseVariable            | This field displays the maximum annual adjustment allowable increase for Variable Charges, based on the increase in the Consumer Price Index. |
| MeterAllowance                         | This field displays the maximum number of miles that can be put on the given unit on a given contract.                                        |
| MeterReading                           | This field displays the current meter reading for the given unit.                                                                             |
| MinAnnualMeter                         | This field displays the minimum annual reading on the given unit.                                                                             |
| Model                                  | This field displays the model of the given unit.                                                                                              |
| ProductionYear                         | This field displays the production year of the given unit.                                                                                    |
| MonthsBeforeCPICalculated              | This field displays the time, in months, before any Consumer Price Index increases can take hold.                                             |
| IsNoReturnDate                         | This field displays that a unit on a contract does not have a return date.                                                                    |
| OriginalUnit                           | This field displays the unit number that the given unit is being substituted for.                                                             |
| OutDate                                | This field displays the date on which a contract began.                                                                                       |
| ParentUnitNumber                       | This field displays the number(s) attached to any parents units.                                                                              |
| PhysicalDamangeInsuranceExpirationDate |                                                                                                                                               |
| PhysicalDamageInsurancePolicyNumber    | This field displays the customer's physical damage insurance policy number.                                                                   |
| PhysicalDamageInsuranceProvider        |                                                                                                                                               |
| PreviouslyBilledMeter                  | This field displays the meter reading at the time billing last occurred for the given unit.                                                   |
| ReturnBranch                           | This field displays the branch where a unit will be returned.                                                                                 |
| ReturnDate                             | This field displays the time when a unit on a contract is due back.                                                                           |
| UserName                               | This field displays the user name assigned as the salesperson on the given contract.                                                          |
| StaringCPI                             | This field displays the Consumer Price Index at the time a unit became active on a contract.                                                  |
| StartingMeter                          | This field displays the starting meter for the given unit on a contract.                                                                      |
| SubUnit                                | This field displays whether the given unit is acting as a substitute for another unit.                                                        |
| IsSubjectToCPI                         | This field displays whether or not a unit is subject to Consumer Price Index increases.                                                       |
| SubsAllowed                            | This field displays whether the given unit is able to be substituted with another unit.                                                       |
| Term                                   | This field displays the customer's payment terms for invoices.                                                                                |
| TotalBilledMeter                       | This field displays the Total Billed Meter for the given unit (running total of meter intervals).                                             |
| UnitIndicator                          | This field displays the unit's unit indicator.                                                                                                |
| UnitNumber                             | This field displays the ID number of a unit attached to a given note.                                                                         |
| LeaseContractUnitStatus                | This field displays the status of the given unit on the contract.                                                                             |
| Vin                                    | This field displays the Vehicle Identification Number.                                                                                        |

---
---
### Lease Rental Contract Unit Charge
---

This data object is used to return charges attached to lease, rental, or
maintenance contracts. 

This can be found in the L/R Contract program in the Fusion business system.

 <!-- SQL VIEW:  **vwLR_SSR_LRContractUnitCharge**



 -->  <hr>Field Details...

| **SQL Field Name**    | **Column Description**                                                                  |
|---|---|
| AddDate               | This field displays the date and time the given record was added to the system.         |
| AddUser               | This field displays the user name that added the record.                                |
| BillingRateFrequency  | This field displays the billing frequency of the given charge.                          |
| Charge                | This field displays the charge for the given unit.                                      |
| ContractNumber        | This field displays the number attached to a contract.                                  |
| Cost                  | This field displays the cost of the charge.                                             |
| Description           | This field displays the description of the given charge.                                |
| LastUpdateDate        | This field displays that date and time the given record was last updated in the system. |
| UpdateUser            | This field displays the user name of the individual who made the last update.           |
| LeaseRentalChargeType | This field displays the type of charge on a contract.                                   |
| MeterType             | This field displays the given unit's meter type (gallons, hours, kilometers, etc.).     |
| OverrideDescription   | This field displays the override description of the charge that the user has input.     |
| Rate                  | This field displays the rate for the given charge.                                      |
| UnitNumber            | This field displays the identification number assigned to the given unit.               |

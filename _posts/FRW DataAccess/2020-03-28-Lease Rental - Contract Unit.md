---
layout: post
title: "Lease - Rental Contract Unit"
category: "Lease / Rental" 
icon: "icon-user-plus1"
type: "data_access" 
comments: false
description: Access all information from a unit on a lease or rental contract from within the Fusion business system
---

---
---

This data object is used to return all information from a unit on a lease or rental contract from within the Fusion business system.

This is found within the Lease Rental Contract Unit program within the Fusion business system.

 
#### URL 
```
/frw/LRContractUnit
``` 
 <hr>
Field Details...

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
| PhysicalDamangeInsuranceExpirationDate | This field displays the customer's physical damage insurance expiration date   |
| PhysicalDamageInsurancePolicyNumber    | This field displays the customer's physical damage insurance policy number.                                                                   |
| PhysicalDamageInsuranceProvider        | This field displays the customer's physical damage insurance provider     |
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
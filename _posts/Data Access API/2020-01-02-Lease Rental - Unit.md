---
layout: post
title: "Lease - Rental Unit"
category: "Lease / Rental" 
icon: "icon-user-plus1"
type: "data_access" comments: falsedescription: Access all all lease or rental unit information
---

---

This data object is used to return all lease or rental unit information.

This information is found within the Unit program within the Fusion business
system.

 <!-- SQL VIEW:  **vwLR_SSR_LRUnits**



 -->  <hr>Field Details...

| **SQL Field Name**          | **Column Description**                                                                                                                                   |
|---|---|
| AddDate                     | This field displays the date in which the unit was added to the Fusion System.                                                                           |
| AddUser                     | This field displays the user name that added the record.                                                                                                 |
| BillingMeterReading         | This field displays the current Billing Meter for the given Lease Rental Unit.                                                                           |
| BillingMeterReadingDate     | This displays the date on which the current Billing Meter for the given unit was captured.                                                               |
| CharacteristicType          | This field displays the unit's characteristic type (truck, trailer, reefer, etc.).                                                                       |
| CurrentLRContract           | This field contains the current lease rental contract number the unit is active on.                                                                      |
| CurrentLRContractBranch     | This field displays the branch associated with the given unit's current contract.                                                                        |
| CurrentLRContractCustomer   | This field displays the company name of the customer associated with the unit's current contract.                                                        |
| CurrentLRContractOutDate    | This field displays the date in which the unit went out for its current contract.                                                                        |
| CurrentLRContractReturnDate | This field displays the date in which the unit will be returned for its current contract.                                                                |
| EquipmentClass              | This field displays the Equipment Class assigned to the given unit.                                                                                      |
| EquipmentType               | This field displays the Equipment Type assigned to the given unit.                                                                                       |
| FinanceSource               | This field displays the lease rental finance source for the given unit.                                                                                  |
| FirstTaxableUse             | This field displays the unit's First Taxable Use date.                                                                                                   |
| FleetNumber                 | This field displays the Fleet number assigned to the given unit.                                                                                         |
| FleetType                   | This field displays the Fleet Type assigned to the given unit.                                                                                           |
| GVWR                        | This field displays the Gross Vehicle Weight Rating of the given unit.                                                                                   |
| CustomerKey                 | This field displays the internal customer number assigned to the given unit.                                                                             |
| LastUpdateDate              | This field displays the date in which the unit was added to the Fusion System.                                                                           |
| LastUpdateUser              | This field displays the username who last updated the record.                                                                                            |
| LocationBranchCode          | This field displays the branch where a fleet is located.                                                                                                 |
| LotLocation                 | This field displays the lot location assigned to the given unit.                                                                                         |
| LotLocationBranch           | This field dislays the branch associated with the given unit's lot location.                                                                             |
| RentalRate                  | This field displays the default L/R rate table assigned to the given unit.                                                                               |
| LRUnitMessage               | This field displays the message in the Comments box from the Unit form on the Lease/Rental tab.                                                          |
| LRUnitStatus                | This field displays the current status of the given unit.                                                                                                |
| Make                        | This field displays the make of a given L/R Unit.                                                                                                        |
| Manufacturer                | This field displays the manufacturer of a given L/R Unit.                                                                                                |
| MeterReading                | This field displays the current meter reading for a lease or rental unit.                                                                                |
| MeterType                   | This field displays the unit's meter type (gallons, hours, kilometers, etc.).                                                                            |
| Model                       | This field displays the model of the given L/R unit.                                                                                                     |
| OwningBranchCode            | This field displays the Owning Branch of the given unit.                                                                                                 |
| PrimaryLicenseNumber        | This field displays the primary license number assigned to the given unit.                                                                               |
| ProductionYear              | This field displays the model year of a given L/R Unit.                                                                                                  |
| RegisteredWeight            | This field displays the unit's Registered Weight.                                                                                                        |
| RegisteredWeightCategory    | This field displays the unit's Registered Weight Category.                                                                                               |
| IsRepairOrderComment        | This field determines whether or not the message typed in on the unit record appears as a display message when that unit is validated on a repair order. |
| IsSaleUnit                  | This field displays whether or not a unit is flagged as a sales unit.                                                                                    |
| SerialNumber                | This field displays the serial number of a given L/R unit.                                                                                               |
| UnitIndicator               | This field displays the type of unit (sales, service, lease/rental, etc.).                                                                               |
| UnitNumber                  | This field displays the Unit number assigned to the given unit.                                                                                          |
| Vin                         | This field displays the Vehicle Identification Number of a given L/R Unit.                                                                               |

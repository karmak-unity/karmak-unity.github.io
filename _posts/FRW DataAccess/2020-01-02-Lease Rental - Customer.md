---
layout: post
title: "Lease - Rental Customer"
category: "Lease / Rental" 
icon: "icon-user-plus1"
type: "data_access" comments: falsedescription: Access all customer information related to lease / rentals
---

---
---
### Lease Rental Customer Insurance
---

This data object is used to return all customer insurance information from the Fusion business system.

This is found within the Lease Rental Customer Insurance program within the Fusion business system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**            | **Column Description**                                                                 |
|---|---|
| AddDate                       | This field displays the date and time the given record was entered.                    |
| AddUser                       | This field displays the user name that added the record.                               |
| Address1                      | This field displays line one of an insurance agent's address.                          |
| Address2                      | This field displays line two of an insurance agent's address.                          |
| AgentName                     | This field displays the insurance agent's name.                                        |
| City                          | This field displays the insurance provider's city.                                     |
| DamageCollisionCoverage       | This field displays the coverage amount for collision.                                 |
| DamageCollisionDeductible     | This field displays the deductible amount for collision.                               |
| CompanyName                   | This field displays the company name of the customer assigned to the insurance record. |
| IsCompanyProvidedInsurance    | This field displays if the insurance is provided by the company or not.                |
| DamageComprehensiveCoverage   | This field displays the coverage amount for comprehensive.                             |
| DamageComprehensiveDeductible | This field displays the deductible amount for comprehensive.                           |
| CustomerNumber                | This field displays the identifying number attached to a customer.                     |
| Email                         | This field displays the insurance provider's email address.                            |
| ExpirationDate                | This field displays the date on which a customer's insurance policy expires.           |
| Inactive                      | This field displays whether or not a given insurance record is set to inactive.        |
| LastUpdateDate                | This field displays the last update date and time of the given record.                 |
| UpdateUser                    | This field displays the user name of the individual who made the last update.          |
| LiablityCoverage              | This field displays the coverage amount for liability.                                 |
| LiablityDeductible            | This field displays the deductible amount for liability.                               |
| OfficePhone                   | This field displays the insurance agent's office phone number.                         |
| PhysicalDamageCoverageLimit   | This field displays the coverage limit value for Physical Damage policies.             |
| PolicyNumber                  | This field displays the customer's insurance policy number.                            |
| PostalCode                    | This field displays the insurance provider's postal code.                              |
| Description                   | This field displays the description of a given insurance record.                       |
| InsuranceProvider             | This field displays the name of a customer's insurance provider.                       |
| ProviderType                  | This field displays the provider type for the given customer insurance record.         |
| Region                        | This field displays the insurance provider's region or state.                          |
| StartDate                     | This field displays the start date of the given customer insurance policy.             |

---
---
### Lease Rental Driver Info
---

This data object displays the Driver information as seen in the Driver
Information application in Fusion.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name** | **Column Description**                                                                          |
|---|---|
| AddDate            | This field displays the date and time the given record was entered.                             |
| AddUserName        | This field displays the user name that added the record.                                        |
| City               | This field displays the city of the driver license record.                                      |
| CompanyName        | This field displays the company name of the customer assigned to the driver information record. |
| Country            | This field displays the customer's country.                                                     |
| County             | This field displays the customer's county.                                                      |
| CustomerKey        | This field displays the customer number associated with the given record.                       |
| DateOfBirth        | This field displays the date of birth appearing on a driver's license.                          |
| DriverName         | This field displays the driver's name.                                                          |
| ExpirationDate     | This field displays the date on which a customer's license expires.                             |
| FirstName          | This field displays the driver's first name.                                                    |
| Inactive           | This field displays whether or not a given driver record is set to inactive.                    |
| LastName           | This field displays the driver's last name.                                                     |
| LastUpdateDate     | This field displays the last update date and time of the given record.                          |
| UpdateUserName     | This field displays the user name of the individual who updated driver information.             |
| LicenseNumber      | This field displays the driver's license number.                                                |
| Region             | This field displays the region or state associated with the given driver record.                |
| MiddleInitial      | This field displays the driver's middle initial.                                                |
| WorkPhone          | This field displays the driver's phone number.                                                  |
| PostalCode         | This field displays the driver's postal code.                                                   |
| Region1            | This field displays the driver's region or state.                                               |
| Street1            | This field displays line one of the street address for the driver.                              |
| Street2            | This field displays line two of the street address for the driver.                              |
| Type               | This field displays the classification of the license.                                          |

---
---
### Lease Rental Charges
---

This data object is used to return lease rental charge information from the
Fusion business system.

This information is pulled from the Lease Rental Miscellaneous, Fixed, and
Variable Charge programs within the Fusion business system.

 <!-- 


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
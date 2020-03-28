---
layout: post
title: "Lease Rental Charges"
category: "Lease / Rental" 
icon: "icon-user-plus1"
type: "data_access" 
comments: false
description: Access to lease rental charge information from the Fusion business system
---

---
---

This data object is used to return lease rental charge information from the Fusion business system.

This information is pulled from the Lease Rental Miscellaneous, Fixed, and Variable Charge programs within the Fusion business system.

 
#### URL 
```
/frw/LRCharges
``` 
 <hr>
Field Details...

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
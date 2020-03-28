---
layout: post
title: "Service Unit Owning Customer"
category: "Service"
icon: "icon-truck"
type: "data_access" 
comments: false
description: Access to the owning customer(s) of all Service units
---
---


This data object is used to display the owning customer(s) of all Service units. In the case of units with dual ownership, a record will be returned for each customer corresponding to that unit.

This information comes from the Service tab in the Unit application in Fusion, and for units with dual ownership, the Service Unit Customer Maintenance application, which can be opened by clicking the Service Unit Customer Legacy Links hyperlink on the Service tab.

### URL
```
/frw/UnitOwningCustomer
```


<hr>
Field Details...

| **SQL Field Name**        | **Column Description**                                                                                           |
|---|---|
| AddDate                   | This field displays the date on which the given owning customer was added to the given unit.                     |
| AddUser                   | This field displays the username of the user who added the given owning customer to the given unit.              |
| CharacteristicType        | This field displays the characteristic type of the given unit.                                                   |
| CompanyName               | This field displays the company name of the given owning customer of the given unit.                             |
| CustomerBaseBranch        | This field displays the base branch associated with the given owning customer of the given unit.                 |
| CustomerNumber            | This field displays the customer number of the given owning customer of the given unit.                          |
| Inactive                  | This field displays whether the given unit is marked as inactive in Fusion.                                      |
| IndustryType              | This field displays the industry type of the given owning customer of the given unit.                            |
| LastUpdateDate            | This field displays the date on which the given owning customer was last updated on the given unit.              |
| LastUpdateUser            | This field displays the username of the user who last updated the given owning customer on the given unit.       |
| Make                      | This field displays the make of the given unit.                                                                  |
| Manufacturer              | This field displays the manufacturer of the given unit.                                                          |
| Model                     | This field displays the model of the given unit.                                                                 |
| OutsidePartsSalesperson   | This field displays the outside parts salesperson associated with the given owning customer of the given unit.   |
| OutsideServiceSalesperson | This field displays the outside service salesperson associated with the given owning customer of the given unit. |
| UnitNumber                | This field displays the unit number of the given unit that is owned by the given customer.                       |
| VIN                       | This field displays the vehicle identification number of the given unit.                                         |
| Year                      | This field displays the model year of the given unit.                                                            |

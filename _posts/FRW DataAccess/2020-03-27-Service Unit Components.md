---
layout: post
title: "Service Unit Components"
category: "Service"
icon: "icon-truck"
type: "data_access" 
comments: false
description: Access to all Unit Component information for a given unit.
---


---
---

This data object is used to display all Unit Component information for a given unit.  By default, both Active and Inactive Unit Occurrences that contain Component information are returned.

This information can be found on the Component tab of Unit Maintenance within the Fusion Business System. 


### URL
```
/frw/UnitComponents
```
 <hr>
Field Details...

| **SQL Field Name**      | **Column Description**                                                                                            |
|---|---|
| IsActiveUnit            | This displays whether or not the given unit number is the active occurence for the unit.                          |
| AddDate                 | This field displays the user that added the component.                                                            |
| AddUser                 | This field displays the date that the component was added.                                                        |
| ComponentDeactivateDate | This field displays the De-activation date of the component.                                                      |
| ComponentManufacturer   | This field displays the manufacturer of the component.                                                            |
| ComponentModel          | This field displays the model of the component.                                                                   |
| ComponentName           | This field displays the name of the component.                                                                    |
| Description             | This field displays the Description of the Component.                                                             |
| CurrentMeterReading     | This field displays the current meter reading for the unit.                                                       |
| CurrentMeterReadingDate | This field displays the date associated with the current meter reading.                                           |
| Deductible              | This field contains the dollar amount that must be met before the warranty is in effect.                          |
| InServiceDate           | This field displays the in service date of the unit.                                                              |
| LastUpdate              | This field displays the date that the component was updated.                                                      |
| UpdateUser              | This field displays the user that last updated the component.                                                     |
| MeterType               | This displays the meter type of the component.                                                                    |
| PartNumber              | This field displays the part number of the component (if applicable).                                             |
| SerialNumber            | This field displays the serial number of the component.                                                           |
| UnitIndicator           | This field displays the Unit Indicator of the unit the component is associated with.                              |
| UnitNumber              | This field displays the Unit number the component is attached to.                                                 |
| WarrantyContract        | This field displays the document number identifying the warranty agreement between the manufacturer and customer. |
| WarrantyLaborPercentage | This field displays the percentage of labor that is covered by warranty.                                          |
| WarrantyMeter           | This field should contain the number of miles for which the unit is under warranty.                               |
| WarrantyPartPercentage  | This field displays the percentage of parts that are covered by the warranty.                                     |
| WarrantyPeriod          | This field contains the time that the component is covered under warranty.                                        |
| WarrantyPeriodType      | This field defines what the warranty period is for the unit.                                                      |
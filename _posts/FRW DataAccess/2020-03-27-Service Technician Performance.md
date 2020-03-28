---
layout: post
title: "Service Technician Performance"
category : "Service Technician"
icon: "icon-man"
type: "data_access" 
comments: false
description: Access to display technician performance by repair group.
---

---
---

This data object is used to display technician performance by repair group.

This information can be found in the Technician application within the Fusion business system.

 
#### URL
```
/frw/TechnicianPerformance
```

<hr>
Field Details...

| **SQL Field Name**         | **Column Description**                                                                                                                                                     |
|---|---|
| BeginningCalculationDate   | This field displays the date on which performance for the given technician and associated repair group was first calculated to be greater than zero.                       |
| ComebackHours              | This field displays the total number of hours that have had to be worked on repairs after the given technician initially serviced them.                                    |
| EffectiveLaborRate         | This field displays the effective labor rate ((Billed Hours \* Labor Rate)/Productive Hours) for the given technician and repair group.                                    |
| EfficiencyFreezeThruDate   | This field displays the date through which the efficiency calculation for the given technician and associated repair group will be frozen.                                 |
| EfficiencyPercentage       | This field displays the efficiency of the given technician for the given repair group as a percentage, from the Performance tab of the Technician application in Fusion.   |
| GainLossFreezeThruDate     | This field displays the date through which the gain loss calculation for the given technician and associated repair group will be frozen.                                  |
| GainLossPercentage         | This field displays the gain loss of the given technician for the given repair group as a percentage, from the Performance tab of the Technician application in Fusion.    |
| HireDate                   | This field displays the date on which the given technician was hired.                                                                                                      |
| Inactive                   | This field displays whether the given technician has been marked as inactive in Fusion.                                                                                    |
| LastCalculationDate        | This field displays the most recent date on which performance was calculated for the given technician and associated repair group.                                         |
| PaidFlatRate               | This field displays whether the given technician is paid with a flat rate.                                                                                                 |
| PaidIncentive              | This field displays whether the pay for the given technician is affected by incentive bonuses.                                                                             |
| ProductivityFreezeThruDate | This field displays the date through which the productivity calculation for the given technician and associated repair group will be frozen.                               |
| ProductivityPercentage     | This field displays the productivity of the given technician for the given repair group as a percentage, from the Performance tab of the Technician application in Fusion. |
| ProficiencyFreezeThruDate  | This field displays the date through which the proficiency calculation for the given technician and associated repair group will be frozen.                                |
| ProficiencyPercentage      | This field displays the proficiency of the given technician for the given repair group as a percentage, from the Performance tab of the Technician application in Fusion.  |
| RepairGroup                | This field displays the repair group code that the given technician performance values are associated with.                                                                |
| RepairGroupDescription     | This field displays the description of the repair group that the given technician performance values are associated with.                                                  |
| ReviewDate                 | This field displays the most current past review date or scheduled review date for the given technician.                                                                   |
| TechnicianBaseBranch       | This field displays the base branch location for the given technician.                                                                                                     |
| TechnicianBaseDepartment   | This field displays the base department location for the given technician.                                                                                                 |
| TechnicianBaseShift        | This field displays the base shift time for the given technician.                                                                                                          |
| TechnicianName             | This field displays the name (first, middle initial, last) of the given technician.                                                                                        |
| TechnicianNumber           | This field displays the identifying code for the given technician.                                                                                                         |
| TechnicianUserName         | This field displays the username for the given technician in Fusion.                                                                                                       |
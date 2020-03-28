---
layout: post
title: "Service Technician Productivity"
category : "Service Technician"
icon: "icon-man"
type: "data_access" 
comments: false
description: Access to view how productive a technician has been, summarized by month.
---

---
---

### Service Technician Productivity
---

This data object is used to display how productive a technician has been, summarized by month.

This information can be found in the Technician program within the Fusion business system.

#### URL
```
/frw/TechnicianProductivity
``` 
 
<hr>
Field Details...

| **SQL Field Name**       | **Column Description**                                                                                                                                          |
|---|---|
| BilledHours              | This field displays the total number of hours billed for the given month/year combiniation.                                                                     |
| ComebackHours            | This field displays the total number of comeback hours a technician has worked for the given month/year combination.                                            |
| EffectiveRate            | This field displays the technician's effective rate for the given month/year combiniation (Billed Hours \* Labor Rate / Productive Hours).                      |
| EfficiencyPercentage     | This field displays the technician's calculated efficiency percentage for the given month/year combination (Billed hours / Productive hours).                   |
| GainLossPercentage       | This field displays the technician's calculated gain/loss percentage for the given month/year combination (Billed hours / total hours worked).                  |
| Inactive                 | This field displays whether or not a given technician is set to inactive.                                                                                       |
| Month                    | This field displays the name of the month productivity figures are being displayed for.                                                                         |
| MonthNumber              | This field displays the month number producivity figures are being displayed for.                                                                               |
| NonProductiveHours       | This field displays the number of non productive hours a technician has worked for the given month/year combination.                                            |
| ProductiveHours          | This field displays the number of productive hours a technician has worked for the given month/year combination.                                                |
| ProductivityPercentage   | This field displays the technician's productivity percentage for the given month/year combination (Productive hours / total hours worked).                      |
| ProficiencyPercentage    | This field displays the technician's calculated proficiency percentage for the given month/year combination (Billed hours - comeback hours / productive hours). |
| TechnicianBaseBranch     | This field displays the technician's main branch location.                                                                                                      |
| TechnicianBaseDepartment | This field displays the given technician's base department.                                                                                                     |
| TechnicianBaseShift      | This field displays the shift assigned to the given technician.                                                                                                 |
| TechnicianName           | This field displays the technician's name.                                                                                                                      |
| TechnicianNumber         | This field displays the number assigned to a technician.                                                                                                        |
| TotalWorkedHours         | This field displays the technician's total hours worked for the given month/year combination (productive hours + non productive hours).                         |
| Year                     | This field displays the year productivity figures are being displayed for.                                                                                      |
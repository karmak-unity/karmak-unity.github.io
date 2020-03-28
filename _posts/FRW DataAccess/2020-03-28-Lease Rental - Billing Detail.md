---
layout: post
title: "Lease Rental Billing History Detail"
category: "Lease / Rental" 
icon: "icon-user-plus1"
type: "data_access" 
comments: false
description: Display the detail for all charges associated with a given unit on an LR invoice from the Fusion business system
---

---
---

This data object is used to return the detail for all charges associated with a given unit on an LR invoice from the Fusion business system.

This is found within the Lease Rental Billing History program in the Fusion business system.

 
#### URL 
```
/frw/LRBillingHistoryDetail
``` 

<hr>
Field Details...

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


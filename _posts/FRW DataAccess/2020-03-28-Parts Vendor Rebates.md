---
layout: post
title: "Parts Vendor Rebates"
category: "Parts" 
icon: "icon-gear"
type: "data_access" 
comments: false
description:  Display all vendor rebate information
---

---
---

This data object is used to display all vendor rebate information.

This information can be found in the Vendor Rebate program within the Fusion business system.

 
#### URL 
```
/frw/PartsVendorRebates
``` 
 <hr>
Field Details...

| **SQL Field Name**                     | **Column Description**                                                                                                                                                                                           |
|---|---|
| AddUser                                | This field displays the user name that added the record.                                                                                                                                                         |
| AverageCost                            | This field displays the average cost of a given part.                                                                                                                                                            |
| Branch                                 | This field displays the branch associated with the rebate.                                                                                                                                                       |
| CalculateCommissionsBasedOnRebatedCost | This field indicates salesman commission will be calculated based on the rebated cost of the transaction. This field will always be set with the same setting as the Use Rebated Cost at Time of Sale check box. |
| Code1                                  | This field displays the Code 1 field of a part record.                                                                                                                                                           |
| Code2                                  | This field displays the Code 2 field of a part record.                                                                                                                                                           |
| Code3                                  | This field displays the Code 3 field of a part record.                                                                                                                                                           |
| Code4                                  | This field displays the Code 4 field of a part record.                                                                                                                                                           |
| Code5                                  | This field displays the Code 5 field of a part record.                                                                                                                                                           |
| Customer                               | This field displays the customer attached to the given vendor rebate.                                                                                                                                            |
| CustomerName                           | This field displays the customer's name from the customer record.                                                                                                                                                |
| CustomerPricingType                    | This field indicates the customer pricing type for the rebate record.                                                                                                                                            |
| ExpirationDate                         | This field displays the date on which the given rebate expires.                                                                                                                                                  |
| ExtendedRebateAmount                   | This field contains the extended rebate amount (Quantity \* Rebate Amount).                                                                                                                                      |
| InsideSalesperson                      | This field displays the inside salesperson attached to the rebate.                                                                                                                                               |
| InvoiceDate                            | This field displays the invoice date of the parts order associated with the rebate record.                                                                                                                       |
| InvoiceNumber                          | This field displays the invoice number of the parts order associated with the given rebate record.                                                                                                               |
| LastUpdate                             | This field displays the date on which the give rebate was last updated.                                                                                                                                          |
| UpdateUser                             | This field displays the user name of the individual who made the update.                                                                                                                                         |
| Multiplier                             | This field contains the multiplier used to calculate the amount of the rebate.                                                                                                                                   |
| OutsideSalesperson                     | This field displays the outside salesperson who is attached to a given rebate invoice.                                                                                                                           |
| PartDescription                        | This field displays the description of the part that is being rebated.                                                                                                                                           |
| PartNumber                             | This field displays the part number of the part being rebated.                                                                                                                                                   |
| PriceFileSource                        | This field contains the source of the price file used to calculate the rebate.                                                                                                                                   |
| PriceLevel                             | This field contains the price level used to calculate the rebate (List, Price 1-7, Replacement Cost).                                                                                                            |
| Quantity                               | This field displays the quantity sold for a given item.                                                                                                                                                          |
| RebateAmount                           | This field contains the rebate amount.                                                                                                                                                                           |
| RecordNotes                            | This field contains notes that describe the rebate.                                                                                                                                                              |
| ReplacementCost                        | This field displays the replacement cost of a given part.                                                                                                                                                        |
| SellingPrice                           | This field displays the selling price of a given part.                                                                                                                                                           |
| StockClass                             | This field displays a subset within a supplier, typically used in pricing and typically provided by the manufacturer.                                                                                            |
| Supplier                               | This field displays the supplier of the rebated part.                                                                                                                                                            |
| UseRebatedCostAtTimeOfSale             | This setting indicates whether the rebate amount was used to calculate the cost of the transaction.                                                                                                              |
| ValuePriceLevel                        | This field contains the price the rebate was calculated from if it was calculated from an inventory price.                                                                                                       |
| Vendor                                 | This field displays the vendor attached to a given rebate invoice.                                                                                                                                               |
| VendorPrice                            | This field contains the price the rebate was calculated from if it was calculated from a price file price.                                                                                                       |
| VendorPriceDescription                 | This field contains a description of the vendor price from the price file used to calculate the rebate.                                                                                                          |

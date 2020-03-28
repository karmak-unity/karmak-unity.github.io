---
layout: post
title: "Parts Committed"
category: "Parts" 
icon: "icon-gear"
type: "data_access" 
comments: false
description: Display all parts that have been committed on parts order, repair orders, and inter-branch orders
---

---
---

This data object is used to display all parts that have been committed on parts order, repair orders, and inter-branch orders.

 
#### URL 
```
/frw/PartsCommitted
``` 
 <hr>
Field Details...

| **SQL Field Name**      | **Column Description**                                                                                                                                                                                                                                                      |
|---|---|
| IsAssemblyDetail        | This field displays whether or not the given committed part is part of an assembly.                                                                                                                                                                                         |
| AssemblyPartNumber      | This field displays the assembly part number the given part is associated with.                                                                                                                                                                                             |
| AverageCost             | This field displays the average cost of the part at the time it was committed to the order.                                                                                                                                                                                 |
| Branch                  | This field displays the branch the part is committed in.                                                                                                                                                                                                                    |
| CommittedDate           | This field displays the date on which parts were committed.                                                                                                                                                                                                                 |
| CustomerNumber          | This field displays the identifying number attached to a customer.                                                                                                                                                                                                          |
| CompanyName             | This field displays the company name of the customer associated with the order.                                                                                                                                                                                             |
| ExtendedAverageCost     | This field displays the extended average cost of the part at the time it was committed to the order.                                                                                                                                                                        |
| ExtendedReplacementCost | This field displays the extended replacement cost of the part at the time it was committed to the order.                                                                                                                                                                    |
| ExtendedSellingPrice    | This field displays the extended selling price of the given part on the given order.                                                                                                                                                                                        |
| Module                  | This field displays the module the comitted part originated from.  Orders with a module of "Service" originate from Repair Orders.  Orders with a module of "Parts" originate from Parts Orders. Orders with a module of "P/O" originate from inter-branch purchase orders. |
| OrderNumber             | This field displays the order number the part is committed on.                                                                                                                                                                                                              |
| Description             | This field displays the description of a given part.                                                                                                                                                                                                                        |
| PartNumber              | This field displays the part number of the committed part.                                                                                                                                                                                                                  |
| PartType                | This field displays the part type (Part, EXC, INH, or RET) of the given part.                                                                                                                                                                                               |
| Quantity                | This field displays the quantity requested for a given item.                                                                                                                                                                                                                |
| SellingCost             | This field displays the replacement cost of the given part at the time the part was committed to the order.                                                                                                                                                                 |
| RequestingBranch        | This field displays the branch that has requested the part.                                                                                                                                                                                                                 |
| SellingPrice            | This field displays the selling price of a given part.                                                                                                                                                                                                                      |
| SupplierCode            | This field displays the supplier associated with the committed part.                                                                                                                                                                                                        |

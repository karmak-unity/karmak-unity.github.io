---
layout: post
title: "Parts Supplier Core RTR"
category: "Parts" 
icon: "icon-gear"
type: "data_access" 
comments: false
description: Display all supplier core right to return records
---

---
---

This data object is used to show all supplier core right to return records.

This information is located in the Supplier Core Right to Return program in the Fusion business system.

 
#### URL 
```
/frw/SupplierCoreRTR
``` 
 <hr>
Field Details...

| **SQL Field Name**               | **Column Description**                                                                                       |
|---|---|
| AddDateTime                      | This field displays the date on which the record was added.                                                  |
| AddUser                          | This field displays the user name that added the record.                                                     |
| APVendor                         | This field displays the A/P vendor.                                                                          |
| APVendorName                     | This field displays the name of an  Accounts Payable vendor associated with a customer core right to return. |
| BranchCode                       | This field displays the code identifying a branch associated with an Accounts Receivable invoice.            |
| Description                      | This field displays the description of a given part.                                                         |
| PartNumber                       | This field displays the core part number the customer has the right to return.                               |
| CoreRightToReturnDaysSupplier    | This field displays the number of days a customer has to return a core before the right to return expires.   |
| CoreSupplier                     | This field displays the supplier of a core part associated with an exchange part.                            |
| ExpirationDate                   | This field displays the date on which the customer's right to return expires.                                |
| LastUpdateTime                   | This field displays the last date and time the record was updated.                                           |
| UpdateUser                       | This field displays the user name of the individual who made the update.                                     |
| PostingReference                 | This field displays the posting reference number attached to an invoice.                                     |
| QuantityAvailable                | This field displays the quantity available of a certain part.                                                |
| QuantityReceived                 | This field displays the quantity of a part received.                                                         |
| QuantityRemaining                | This field displays the number of cores owed for the given supplier.                                         |
| QuantityReturned                 | This field displays the quantity of a core returned.                                                         |
| ReceivedCost                     | This field displays the cost of a part at the time of receiving.                                             |
| ReceivedDate                     | This field displays the date on which a purchase order was received.                                         |
| TotalOwedForPartNumber           | This field displays the number of cores owed for the given part number.                                      |
| TotalOwedToAPVendorForPartNumber | This field displays the number of cores owed for the given part number for a given AP Vendor.                |

---
layout: post
title: "Parts Customer Backorders"
category: "Parts" 
icon: "icon-gear"
type: "data_access" 
comments: false
description: Display all parts that are backordered on a parts order or repair order
---

---
---

This data object is used to show all parts that are backordered on a parts order or repair order.

This information can be found in the Parts Order and Repair Order programs within the Fusion business system.

 
#### URL 
```
/frw/PartsBackOrders
``` 
 <hr>
Field Details...

| **SQL Field Name**  | **Column Description**                                                                                                |
|---|---|
| AddDate             | This field displays the date on which the back order was created.                                                     |
| AddUser             | This field displays the user name that added the record.                                                              |
| Street1             | This field displays line one of the street address for the customer.                                                  |
| Street2             | This field displays line two of the street address for the customer.                                                  |
| APVendor            | This field displays the A/P vendor.                                                                                   |
| APVendorName        | This field displays the name of an  Accounts Payable vendor associated with a customer core right to return.          |
| BackorderAging      | This field displays the aging category the part falls into based on the Add Date of the part to the order.            |
| BackorderDate       | This field displays the date on which a part was backordered.                                                         |
| BackorderPriority   | This field displays the backorder priority flag assigned to the parts.                                                |
| Quantity            | This field displays the quantity requested for a given item.                                                          |
| Status              | This field displays the status of a given backorder.                                                                  |
| BranchCode          | This field displays the branch that requested the order.                                                              |
| City                | This field displays Bill-To city of the customer the back order is associated with.                                   |
| CoreDescription     | This field displays the description of a core associated with a part.                                                 |
| CorePartNumber      | This field displays the number attached to a core part.                                                               |
| CorePrice           | This field displays the price of the inherent core.                                                                   |
| CoreSupplierCode    | This field displays the code attached to a supplier for a core part.                                                  |
| CustomerKey         | This field displays the customer identification number.                                                               |
| CompanyName         | This field displays the company name of the customer associated with the back order.                                  |
| DaysOld             | This field displays the age of a given back ordered part, expressed in number of days.                                |
| Department          | This field displays the department that requested the part.                                                           |
| Description         | This field displays the description of a given part.                                                                  |
| DetailDeliveryDate  | This field displays the expected delivery date of the given back ordered part.                                        |
| FromBranch          | This field displays the filling branch of the given back ordered part.                                                |
| InsideSalesperson   | This field displays the inside salesperson attached to a backorder.                                                   |
| DirectShip          | This field displays whether or not an item will be a direct ship to a given location.                                 |
| LastUpdate          | This field displays the date on which the backorder was last updated.                                                 |
| UpdateUser          | This field displays the user name of the individual who made the update.                                              |
| OrderingDepartment  | This field displays the module, parts or service, that ordered the part.                                              |
| NoCharge            | This field displays whether or not the part was sold as no charge to the customer on a parts or repair order invoice. |
| OriginalCorePrice   | This field displays the original price of the part.                                                                   |
| OriginalPrice       | This field displays the original price of the inherent core.                                                          |
| Salesperson         | This field displays the salesperson attached to a customer.                                                           |
| PartNumber          | This field displays the part number of the part being backordered.                                                    |
| PartTypeDescription | This field displays the description of a part type for a backordered part.                                            |
| ShipComplete        | This field displays whether or not the given backorderd part can be partially filled or not.                          |
| SalesOrderNumber    | This field displays the number attached to a sales order.                                                             |
| PostalCode          | This field displays the customer's postal code.                                                                       |
| Price               | This field displays the price the customer was charged for the part.                                                  |
| PONumber            | This field displays the Parts Purchase Order Number.                                                                  |
| PurchaseOrderStatus | This field displays the order status of the backorder.                                                                |
| QuantityAvailable   | 0                                                                                                                     |
| Region              | This field displays the customer's region or state.                                                                   |
| RepairOrderNumber   | This field displays the number attached to a repair order.                                                            |
| CustomerPONumber    | This field displays the Customer's purchase order number.                                                             |
| SupplierCode        | This field displays the code attached to a supplier for a part.                                                       |
| TaskNumber          | This field displays the number attached to a given task.                                                              |

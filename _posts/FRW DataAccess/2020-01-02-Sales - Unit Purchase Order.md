---
layout: post
title: "Unit Purchase Order"
category: "Sales"
icon: "icon-tag"
type: "data_access"
comments: falsedescription: Access to the unit information on unit purchase orders
---

---

This data object is used to display the unit information on unit purchase orders. Join to Unit Purchase Order Header to view the header level information.

This information can be found in the Sales Purchase Order program within the
Fusion business system.

 <!-- SQL VIEW:  **vwSM_SSR_UnitPurchaseOrderDetail**



 -->  <hr>Field Details...

| **SQL Field Name**          | **Column Description**                                                                                                                                     |
|---|---|
| AcquiringSalesperson        | This field displays the salesperson responsible for acquiring the given unit into inventory.                                                               |
| AcquisitionDate             | This field displays the date on which the given unit was acquired into inventory.                                                                          |
| AcquisitionMethod           | This field displays the method by which the given unit was acquired into inventory.                                                                        |
| ActualShipDate              | This field displays the date on which the given unit was shipped.                                                                                          |
| AddDate                     | This field displays the date on which the given unit was added to the given unit purchase order.                                                           |
| AddUser                     | This field displays the username of the user who added the given unit to the given unit purchase order.                                                    |
| BaseCost                    | This field displays the base cost of the given unit.                                                                                                       |
| Branch                      | This field displays the branch associated with the given unit purchase order.                                                                              |
| BuildDate                   | This field displays the date on which the given unit was scheduled to be built.                                                                            |
| ClosedDate                  | This field displays the date the given purchase order was closed.                                                                                          |
| CurrencyCode                | This field displays the currency code which indicates which currency the cost of the given unit should be converted to.                                    |
| Customer                    | This field displays the customer number of the customer who purchased the given unit.                                                                      |
| CustomerPO                  | This field displays the purchase order number for the customer associated with the deal on which the unit was sold.                                        |
| DealNumber                  | This field displays the deal number of the deal on which the given unit was sold.                                                                          |
| Department                  | This field displays the department associated with the given unit purchase order.                                                                          |
| EstimatedArrivalDate        | This field displays the date on which the given unit was estimated to arrive.                                                                              |
| InventoryType               | This field displays the inventory type of the given unit.                                                                                                  |
| LastUpdateDate              | This field displays the date on which the given unit was last updated on the given unit purchase order.                                                    |
| LastUpdateUser              | This field displays the username of the user who last updated the given unit on the given unit purchase order.                                             |
| Make                        | This field displays the make of the given unit.                                                                                                            |
| Model                       | This field displays the model of the given unit.                                                                                                           |
| OrderDate                   | This field displays the date the given purchase order was placed (defaults to the date it was added to the system, but can be manually changed in Fusion). |
| PODate                      | This field displays the date of the given unit purchase order (defaults to the date it was added to the system, but can be manually changed in Fusion).    |
| PONumber                    | This field displays the purchase order number associated with the given unit purchase order.                                                               |
| PurchasingStatus            | This field displays the status of the given unit purchase order.                                                                                           |
| RequestedShipDate           | This field displays the date on which the given unit was requested to be shipped.                                                                          |
| Salesperson                 | This field displays the salesperson associated with the deal on which the given unit was sold.                                                             |
| SerialNumber                | This field displays the serial number associated with the given unit.                                                                                      |
| StockNumber                 | This field displays the stock number for the given unit.                                                                                                   |
| Supplier                    | This field displays the identifying code for the customer or vendor who is acting as the supplier for the given unit purchase order.                       |
| SupplierName                | This field displays the company name of the customer or vendor who is acting as the supplier for the given unit purchase order.                            |
| UnitShipToAddressCity       | This field displays the city of the ship to address for the unit on the given unit purchase order.                                                         |
| UnitShipToAddressCountry    | This field displays the country of the ship to address for the unit on the given unit purchase order.                                                      |
| UnitShipToAddressCounty     | This field displays the county of the ship to address for the unit on the given unit purchase order.                                                       |
| UnitShipToAddressPostalCode | This field displays the postal code of the ship to address for the unit on the given unit purchase order.                                                  |
| UnitShipToAddressRegion     | This field displays the region of the ship to address for the unit on the given unit purchase order.                                                       |
| UnitShipToAddressStreet1    | This field displays the first line of the ship to address for the unit on the given unit purchase order.                                                   |
| UnitShipToAddressStreet2    | This field displays the second line of the ship to address for the unit on the given unit purchase order.                                                  |
| VIN                         | This field displays the vehicle identification number for the given unit.                                                                                  |
| Year                        | This field displays the year of the given unit.                                                                                                            |

---
---
### Unit Purchase Order Header
---

This data object is used to display the header information on unit purchase
orders. Join to Unit Purchase Order Detail to view the detail level information.

This information can be found in the Sales Purchase Order program within the
Fusion business system.

 <!-- SQL VIEW:  **vwSM_SSR_UnitPurchaseOrderHeader**



 -->  <hr>Field Details...

| **SQL Field Name**              | **Column Description**                                                                                                                                            |
|---|---|
| AddDate                         | This field displays the date on which the given unit purchase order was added to the system.                                                                      |
| AddUser                         | This field displays the username of the user who added the given unit purchase order to the system.                                                               |
| Branch                          | This field displays the branch associated with the given unit purchase order.                                                                                     |
| BranchBillToAddressCity         | This field displays the city of the bill to address for the branch associated with the given unit purchase order.                                                 |
| BranchBillToAddressCountry      | This field displays the country of the bill to address for the branch associated with the given unit purchase order.                                              |
| BranchBillToAddressCounty       | This field displays the county of the bill to address for the branch associated with the given unit purchase order.                                               |
| BranchBillToAddressPostalCode   | This field displays the postal code of the bill to address for the branch associated with the given unit purchase order.                                          |
| BranchBillToAddressRegion       | This field displays the region of the bill to address for the branch associated with the given unit purchase order.                                               |
| BranchBillToAddressStreet1      | This field displays the first line of the bill to address for the branch associated with the given unit purchase order.                                           |
| BranchBillToAddressStreet2      | This field displays the second line of the bill to address for the branch associated with the given unit purchase order.                                          |
| CellPhone                       | This field displays the cell phone for the primary contact at the supplier associated with the given unit purchase order.                                         |
| ClosedDate                      | This field displays the date on which the given unit purchase order was closed.                                                                                   |
| Department                      | This field displays the department associated with the given unit purchase order.                                                                                 |
| EmailAddress                    | This field displays the email address for the primary contact at the supplier associated with the given unit purchase order.                                      |
| FactoryOrderNumber              | This field displays the factory order number associated with the given unit purchase order.                                                                       |
| Fax                             | This field displays the fax for the primary contact at the supplier associated with the given unit purchase order.                                                |
| HomePhone                       | This field displays the home phone for the primary contact at the supplier associated with the given unit purchase order.                                         |
| LastUpdateDate                  | This field displays the date on which the given unit purchase order was last updated in the system.                                                               |
| LastUpdateUser                  | This field displays the username of the user who last updated the given unit purchase order in the system.                                                        |
| Pager                           | This field displays the pager for the primary contact at the supplier associated with the given unit purchase order.                                              |
| PODate                          | This field displays the date of the given unit purchase order (defaults to the date it was added to the system, but can be manually changed in Fusion).           |
| PONumber                        | This field displays the purchase order number associated with the given unit purchase order.                                                                      |
| POTotal                         | This field displays the sum of the base cost of all units on the given unit purchase order.                                                                       |
| POType                          | This field displays the type of the given unit purchase order (Stock or Customer).                                                                                |
| PurchasingStatus                | This field displays the status of the given unit purchase order.                                                                                                  |
| ShipToAddressCity               | This field displays the city of the ship to address for the supplier associated with the given unit purchase order.                                               |
| ShipToAddressCountry            | This field displays the country of the ship to address for the supplier associated with the given unit purchase order.                                            |
| ShipToAddressCounty             | This field displays the county of the ship to address for the supplier associated with the given unit purchase order.                                             |
| ShipToAddressPostalCode         | This field displays the postal code of the ship to address for the supplier associated with the given unit purchase order.                                        |
| ShipToAddressRegion             | This field displays the region of the ship to address for the supplier associated with the given unit purchase order.                                             |
| ShipToAddressStreet1            | This field displays the first line of the ship to address for the supplier associated with the given unit purchase order.                                         |
| ShipToAddressStreet2            | This field displays the second line of the ship to address for the supplier associated with the given unit purchase order.                                        |
| Supplier                        | This field displays the identifying code for the customer or vendor who is acting as the supplier for the given unit purchase order.                              |
| SupplierBillToAddressCity       | This field displays the city of the bill to address for the customer or the remit to address for the vendor associated with the given unit purchase order.        |
| SupplierBillToAddressCountry    | This field displays the country of the bill to address for the customer or the remit to address for the vendor associated with the given unit purchase order.     |
| SupplierBillToAddressCounty     | This field displays the county of the bill to address for the customer or the remit to address for the vendor associated with the given unit purchase order.      |
| SupplierBillToAddressPostalCode | This field displays the postal code of the bill to address for the customer or the remit to address for the vendor associated with the given unit purchase order. |
| SupplierBillToAddressRegion     | This field displays the region of the bill to address for the customer or the remit to address for the vendor associated with the given unit purchase order.      |
| SupplierBillToAddressStreet1    | This field displays the first line of the bill to address for the customer or the remit to address for the vendor associated with the given unit purchase order.  |
| SupplierBillToAddressStreet2    | This field displays the second line of the bill to address for the customer or the remit to address for the vendor associated with the given unit purchase order. |
| SupplierName                    | This field displays the company name of the customer or vendor who is acting as the supplier for the given unit purchase order.                                   |
| SupplierType                    | This field displays the type of the supplier for the given unit purchase order (Vendor or Customer).                                                              |
| TotalUnitsOrdered               | This field displays the number of units ordered total on the given unit purchase order.                                                                           |
| UnitsOutstanding                | This field displays the number of units outstanding (yet to be filled) on the given unit purchase order.                                                          |
| UnitsReceived                   | This field displays the number of units received already on the given unit purchase order.                                                                        |
| WebAddress                      | This field displays the web address for the primary contact at the supplier associated with the given unit purchase order.                                        |
| WorkPhone                       | This field displays the work phone for the primary contact at the supplier associated with the given unit purchase order.                                         |

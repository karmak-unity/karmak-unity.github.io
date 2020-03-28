---
layout: post
title: "Unit Purchase Order Detail"
category: "Sales"
icon: "icon-tag"
type: "data_access"
comments: falsedescription: Access to the unit information detail on unit purchase orders
---

---

This data object is used to display the unit information on unit purchase orders. Join to Unit Purchase Order Header to view the header level information.

This information can be found in the Sales Purchase Order program within the Fusion business system.

### URL
```
/frw/UnitPurchaseOrderDetail
```
<hr>Field Details...

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

---
layout: post
title: "Sales Unit"
category: "Sales"
icon: "icon-tag"
type: "data_access"
comments: false
description: Access to all sales unit records and their characteristics
---
---

This data object is used to display all sales unit records and their characteristics.

This information can be found in the Unit application within the Fusion business system.

#### URL
```
/frw/SalesUnit
```

Field Details...

| SQL Field Name                 | Column Description                                                                                                                                                                                                                              |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AcquiringSalesperson               | This field displays the salesperson responsible for the acquisition of the given unit.                                                                                                                                                              |
| AcquisitionDate                    | This field displays the date on which the given unit was acquired.                                                                                                                                                                                  |
| AcquisitionMethod                  | This field displays the method by which the given unit was acquired and added to inventory.                                                                                                                                                         |
| IsActiveUnit                       | This field displays whether the given unit is active in inventory.                                                                                                                                                                                  |
| ActualCashValue                    | This field displays the actual value of the given trade in unit, at which it will be booked.                                                                                                                                                        |
| ActualShipDate                     | This field displays the date on which the given unit was shipped.                                                                                                                                                                                   |
| AddDate                            | This field displays the date on which the given unit was added to the system.                                                                                                                                                                       |
| AddUser                            | This field displays the user name of the user who added the given unit to the system.                                                                                                                                                               |
| AskingPrice                        | This field displays the dollar amount that is being asked for the given unit.                                                                                                                                                                       |
| AvailabilityStatus                 | This field displays the availability status of the given unit.                                                                                                                                                                                      |
| Barcode                            | This field displays the barcode of the given unit.                                                                                                                                                                                                  |
| BaseCost                           | This field displays the estimated base cost of the unit, before an invoice is received.                                                                                                                                                             |
| BookBranch                         | This field displays the book branch of the given unit.                                                                                                                                                                                              |
| BuildDate                          | This field displays the date on which the given unit was built or will be built.                                                                                                                                                                    |
| CharacteristicType                 | This field displays the characteristic type of the given unit.                                                                                                                                                                                      |
| Consignor                          | This field displays the consignor of the given unit, if the unit was acquired through consignment.                                                                                                                                                  |
| ControlBranch                      | This field displays the control branch of the given unit.                                                                                                                                                                                           |
| ControlDepartment                  | This field displays the control department of the given unit.                                                                                                                                                                                       |
| CurrencyCode                       | This field displays the currency code for the customer associated with the given unit.                                                                                                                                                              |
| CurrentCost                        | This field displays the current cost of the given unit.                                                                                                                                                                                             |
| CurrentECMReading                  | This field displays the most current ECM reading of the unit.                                                                                                                                                                                       |
| CurrentECMReadingDate              | This field displays the date on which the most current ECM reading was recorded.                                                                                                                                                                    |
| CurrentMeterReading                | This field displays the most current meter reading of the unit.                                                                                                                                                                                     |
| CurrentMeterReadingDate            | This field displays the date on which the most current meter reading was recorded.                                                                                                                                                                  |
| CurrentTitleNumber                 | This field displays the current title number of the given unit.                                                                                                                                                                                     |
| DaysInInventory                    | This field displays the number of days that the given unit has been in inventory.                                                                                                                                                                   |
| DaysInInventory-ReceiveDate        | This field displays the number of days that the given unit has been in inventory, based on the receive date of the unit.                                                                                                                            |
| DaysInInventory-ReceiveInvoiceDate | This field displays the number of days that the given unit has been in inventory, based on the invoice date of the unit.                                                                                                                            |
| EstimatedArrivalDate               | This field displays the date on which the given unit is estimated to arrive.                                                                                                                                                                        |
| Export                             | This field displays whether the given unit record can be exported to a file or uploaded to the web.                                                                                                                                                 |
| FactoryOrderNumber                 | This field displays the order number of the given unit order to the factory.                                                                                                                                                                        |
| FETCharged                         | This field displays whether FET taxes are charged on the given unit.                                                                                                                                                                                |
| FETExemptDeliveryExpenses          | This field displays the FET exempt delivery expenses associated with the given unit.                                                                                                                                                                |
| FETExemptEquipment                 | This field displays the FET exempt equipment total associated with the given unit.                                                                                                                                                                  |
| FlooringBalance                    | This field displays the balance (flooring amount - total payments against principle) of the flooring amount for the given unit.                                                                                                                     |
| GVWR                               | This field displays the Gross Vehicle Weight Rating of the given unit.                                                                                                                                                                              |
| Holdback                           | This field displays the amount of the price of the given unit that is held back by the OEM.                                                                                                                                                         |
| InServiceDate                      | This field displays the date on which the given unit went into service.                                                                                                                                                                             |
| InServiceDealerCode                | This field displays the dealer code associated with the warranty on the given unit.                                                                                                                                                                 |
| InServiceMeterReading              | This field displays the meter reading of the given unit at the time its warranty was entered.                                                                                                                                                       |
| Inactive                           | This field displays whether the given unit is inactive.                                                                                                                                                                                             |
| InventoryType                      | This field displays the inventory type of the given unit.                                                                                                                                                                                           |
| InvoicePostedDate                  | This field displays the date on which the invoice for the given unit was posted.                                                                                                                                                                    |
| JournalSequence                    | This field displays the journal sequence associated with the invoice that the unit was received on.                                                                                                                                                 |
| LastUpdateDate                     | This field displays the date on which the given unit was last updated.                                                                                                                                                                              |
| LastUpdateUser                     | This field displays the user name of the user who last updated the given unit.                                                                                                                                                                      |
| IsLeaseRentalUnit                  | This field displays whether the given unit is a lease rental unit.                                                                                                                                                                                  |
| ListPrice                          | This field displays the list price of the given unit.                                                                                                                                                                                               |
| LotLocation                        | This field displays the lot location of the given unit.                                                                                                                                                                                             |
| LowPrice                           | This field displays the lowest asking price listed for the given unit.                                                                                                                                                                              |
| LPO Actual Cost                    | This field displays the actual cost on the local purchase order and is updated when the local purchase order is closed.                                                                                                                             |
| Make                               | This field displays the make of the given unit.                                                                                                                                                                                                     |
| Manufacturer                       | This field displays the manufacturer of the given unit.                                                                                                                                                                                             |
| Max View Date                      | This field displays the latest date on which Unit Inventory, Local Purchase Order, G/L Transaction, or Lot Location was last updated.                                                                                                               |
| MeterType                          | This field displays the meter type of the given unit.                                                                                                                                                                                               |
| Model                              | This field displays the model of the given unit.                                                                                                                                                                                                    |
| NewUnit                            | This field displays whether the given unit is a new unit.                                                                                                                                                                                           |
| OpenLpos                           | This field displays the total expected amount of all LPOs associated with the given unit.                                                                                                                                                           |
| OrderDate                          | This field displays the date on which the given unit was ordered.                                                                                                                                                                                   |
| PeriodType                         | This field displays the units (hours, days, or months) of the warranty period of the given unit.                                                                                                                                                    |
| PONumber                           | This field displays the order number of the purchase order that the given unit is associated with.                                                                                                                                                  |
| PreviousOwner                      | This field displays the company name of the previous owner of the given unit.                                                                                                                                                                       |
| ProductClass                       | This field displays the product class associated with the given unit.                                                                                                                                                                               |
| PurchaseCost                       | This field displays the purchase cost of the given unit.                                                                                                                                                                                            |
| PurchaseOrderStatus                | This field displays the status of the purchase order that the given unit is associated with.                                                                                                                                                        |
| PurchaseUnitStatus                 | This field displays the status of the detail item for the unit on the purchase order that the given unit is associated with.                                                                                                                        |
| ReceiveInvoiceDate                 | This field displays the date on which the invoice for the given unit was received.                                                                                                                                                                  |
| ReceiveInvoiceNumber               | This field displays the invoice number of the invoice that was received for the given unit.                                                                                                                                                         |
| ReceivedDate                       | This field displays the date on which the given unit was received.                                                                                                                                                                                  |
| ReplenishStock                     | This field displays whether the given unit was purchased to replenish stock.                                                                                                                                                                        |
| RequestShipDate                    | This field displays the date on which the given unit was requested to be shipped.                                                                                                                                                                   |
| SellingStatus                      | This field displays the selling status of the given unit.                                                                                                                                                                                           |
| SoldCustomerName                   | This field displays the company name for the customer that bought the given unit.                                                                                                                                                                   |
| SoldCost                           | This field displays the cost of the given unit at the time it was sold.                                                                                                                                                                             |
| SoldCustomerKey                    | This field displays the identifying number for the customer that bought the given unit.                                                                                                                                                             |
| SoldCustomerAddress1               | This field displays the first line from the address for the customer that bought the given unit.                                                                                                                                                    |
| SoldCustomerAddress2               | This field displays the second line from the address for the customer that bought the given unit.                                                                                                                                                   |
| SoldCustomerCity                   | This field displays the city from the address for the customer that bought the given unit.                                                                                                                                                          |
| SoldCustomerCountry                | This field displays the country from the address for the customer that bought the given unit.                                                                                                                                                       |
| SoldCustomerCounty                 | This field displays the county from the address for the customer that bought the given unit.                                                                                                                                                        |
| SoldCustomerPostalCode             | This field displays the postal code from the address for the customer that bought the given unit.                                                                                                                                                   |
| SoldCustomerRegion                 | This field displays the region or state from the address for the customer that bought the given unit.                                                                                                                                               |
| SoldDate                           | This field displays the date on which the given unit was sold.                                                                                                                                                                                      |
| SoldInvoiceNumber                  | This field displays the invoice number of the invoice that was sent when the given unit was sold.                                                                                                                                                   |
| SoldPrice                          | This field displays the price of the given unit at the time it was sold.                                                                                                                                                                            |
| SoldSalesperson                    | This field displays the name of the salesperson who was responsible for the sale of the given unit.                                                                                                                                                 |
| SpecialPrice                       | This field displays the special price of the given unit that the customer may qualify for.                                                                                                                                                          |
| SpecialPriceExpiration             | This field displays the date on which the special price for the given unit expires.                                                                                                                                                                 |
| StockNumber                        | This field displays the stock number of the given unit.                                                                                                                                                                                             |
| TemporaryLocationName              | This field displays the name of the temporary location of the given unit.                                                                                                                                                                           |
| TemporaryLocationType              | This field displays the type of the temporary location of the given unit.                                                                                                                                                                           |
| TireTaxCredit                      | This field displays the tire tax credit assigned to the given unit in the Unit Maintenance form.                                                                                                                                                    |
| TitleRegion                        | This field displays the region or state from which the title of the given unit was issued.                                                                                                                                                          |
| TotalUnitCost                      | This field displays the total cost of the given unit.                                                                                                                                                                                               |
| TradeInAllowance                   | This field displays the total amount offered for the given trade in unit.                                                                                                                                                                           |
| UnitCostConversion                 | This field displays at which point during the selling process the cost of the given unit should be converted from foreign currency to the local currency.                                                                                           |
| UnitCostConverted                  | This field displays whether the Unit Cost Converted checkbox on the Unit Maintenance form for the given unit is selected, which indicates whether the cost of the given unit will need to be converted from foreign currency to the local currency. |
| UnitIndicator                      | This field displays the type of the given unit, Sales or Lease/Rental.                                                                                                                                                                              |
| UsageType                          | This field displays the user defined usage type assigned to the given unit.                                                                                                                                                                         |
| VIN                                | This field displays the Vehicle Identification Number assigned to the given unit.                                                                                                                                                                   |
| VoidOrderDate                      | This field displays the date on which the order for the given unit was voided.                                                                                                                                                                      |
| WarrantyContract                   | This field displays the warranty contract entered on the Warranty tab of the Unit Maintenance form for the given unit.                                                                                                                              |
| WarrantyMeter                      | This field displays the meter reading through which the warranty on the given unit is open.                                                                                                                                                         |
| WarrantyPeriod                     | This field displays the time period through which the warranty on the given unit is open.                                                                                                                                                           |
| Year                               | This field displays the year of the given unit.                                                                                                                                                                                                     |
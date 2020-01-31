---
layout: post
title: "Service Unit"
category: "Service"
icon: "icon-truck"
type: "data_access" comments: falsedescription: Access all unit detail information
---


---
---
### Master Detail Information
---

This data object is used to display all unit master detail information.

This information can be found in the Unit program within the Fusion business
system.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**                | **Column Description**                                                                                                                                                                                                                                    |
|---|---|
| AcquiringSalesperson              | This field displays the salesperson associated with the acquisition of a unit.                                                                                                                                                                            |
| AcquisitionDate                   | This field displays the date on which the unit was acquired.                                                                                                                                                                                              |
| AcquisitionMethod                 | This field displays the method by which a unit is aquired into inventory.                                                                                                                                                                                 |
| IsActiveUnit                      | This displays whether or not the given unit number is the active occurence for the unit.                                                                                                                                                                  |
| ActualCashValue                   | This field displays the actual value of a trade-in unit at which it will be booked into inventory.                                                                                                                                                        |
| ActualShipDate                    | This field displays the date on which a unit was shipped.                                                                                                                                                                                                 |
| AddDate                           | This field displays the date on which the unit was added.                                                                                                                                                                                                 |
| AddUser                           | This field displays the user name that added the record.                                                                                                                                                                                                  |
| AskingPrice                       | This field displays the amount, expressed in dollars that is being asked of for a unit.                                                                                                                                                                   |
| AvailabilityStatus                | This field displays the unit's availability status (Available- In Stock, Not Available, Pending Trade, etc.).                                                                                                                                             |
| Barcode                           | This field displays the bar code attached to a part.                                                                                                                                                                                                      |
| BaseCost                          | This field displays the estimate of an additional unit's cost before an invoice is received.                                                                                                                                                              |
| BillingMeterReading               | This field displays the current Billing Meter for the given Unit.                                                                                                                                                                                         |
| BillingMeterReadingDate           | This displays the date on which the current Billing Meter for the given unit was captured.                                                                                                                                                                |
| BookBranch                        | This field displays the book branch tied to a given Unit.                                                                                                                                                                                                 |
| BuildDate                         | This field displays the date on which a unit was set to be built.                                                                                                                                                                                         |
| CharacteristicType                | This field displays the unit's characteristic type (truck, trailer, reefer, etc.).                                                                                                                                                                        |
| Consignor                         | This field displays, if a unit was aquired through the method of consignement, the consignor of the unit.                                                                                                                                                 |
| ControlBranch                     | This field displays the controlling branch of a given unit.                                                                                                                                                                                               |
| ControlDepartment                 | This field displays the controlling department of a given unit within the controlling branch.                                                                                                                                                             |
| CurrencyCode                      | This field displays the currency code attached to a particular customer account.                                                                                                                                                                          |
| CurrentCost                       | This field displays the cost returned from the Legacy system for schedule detail.                                                                                                                                                                         |
| CurrentECMReading                 | This field displays the ECM reading of the unit.                                                                                                                                                                                                          |
| CurrentECMReadingDate             | This field displays the date the ECM reading was last updated.                                                                                                                                                                                            |
| CurrentMeterReading               | This field displays the current meading reading of the unit.                                                                                                                                                                                              |
| CurrentMeterReadingDate           | This field displays the date the meter reading was last updated.                                                                                                                                                                                          |
| CurrentTitleNumber                | This field displays the Current Title Number for the unit.                                                                                                                                                                                                |
| DaysInInventory                   | This field displays the number of days the unit has been in inventory.                                                                                                                                                                                    |
| DaysInInventoryReceiveDate        | This field displays the Days the Unit has been in Inventory based off of the Receive Date of the unit.                                                                                                                                                    |
| DaysInInventoryReceiveInvoiceDate | This field displays the Days the Unit has been in Inventory based off of the Invoice Date of the unit.                                                                                                                                                    |
| DueForServiceBranch               | This field displays the branch in which the unit is due for preventive maintenance.                                                                                                                                                                       |
| EquipmentClass                    | This field displays the equipment class of the given unit.                                                                                                                                                                                                |
| EquipmentType                     | This field displays the equipment type of the given unit.                                                                                                                                                                                                 |
| EstimatedArrivalDate              | This field displays the Estimated Arrival Date of the unit.                                                                                                                                                                                               |
| Export                            | This field is a flag to denote whether or not the Unit record can be exported (uploaded) to a website, etc.                                                                                                                                               |
| FactoryOrderNumber                | This field displays the number tied to a placed Factory Order.                                                                                                                                                                                            |
| FETCharged                        | This field displays whether or not FET is charged on the unit.                                                                                                                                                                                            |
| FETExemptDeliveryExpenses         | This field displays any FET Exempt Delivery Expenses if it has been entered.                                                                                                                                                                              |
| FETExemptEquipment                | This field displays the FET Exempt Equipment amount if it has been entered.                                                                                                                                                                               |
| FleetType                         | This field displays the fleet type of the given unit.                                                                                                                                                                                                     |
| FlooringBalance                   | This field displays the flooring amount minus all principal payments.                                                                                                                                                                                     |
| GVWR                              | This field displays the Gross Vehicle Weight Rating (GVWR) of the Unit.                                                                                                                                                                                   |
| InServiceDate                     | This field displays the date on which an asset went into service.                                                                                                                                                                                         |
| InServiceDealerCode               | This field displays the Warranty In Service Dealer Code.                                                                                                                                                                                                  |
| InServiceMeterReading             | This field displays the Warranty In Service Meter Reading.                                                                                                                                                                                                |
| Inactive                          | This field displays whether or not a given unit is set to inactive.                                                                                                                                                                                       |
| InventoryType                     | This field displays the unit's inventory type (new truck, used truck, etc.).                                                                                                                                                                              |
| LastUpdateDate                    | This field displays the date the given unit was last updated.                                                                                                                                                                                             |
| LastUpdateUser                    | This field displays the user name of the person who last updated the unit record.                                                                                                                                                                         |
| ListPrice                         | This field displays either a user's list price or a manufacturer's list price.                                                                                                                                                                            |
| LocationBranch                    | This field displays the location branch of a given asset.                                                                                                                                                                                                 |
| LotLocation                       | This field displays the location of a unit.                                                                                                                                                                                                               |
| LowPrice                          | This field displays the lowest asking price, expressed in dollars, listed for a unit.                                                                                                                                                                     |
| Make                              | This field displays the make of a given unit.                                                                                                                                                                                                             |
| Manufacturer                      | This field displays the manufacturer of a given unit.                                                                                                                                                                                                     |
| MeterType                         | This field displays the unit's meter type (gallons, hours, kilometers, etc.).                                                                                                                                                                             |
| Model                             | This field displays the model of a given unit.                                                                                                                                                                                                            |
| NewUnit                           | This field displays whether or not a unit is new.                                                                                                                                                                                                         |
| OpenLpos                          | This field displays the sum of the expected amount of all LPOs whose purchasing status is "Open".                                                                                                                                                         |
| OrderDate                         | This field displays the Order Date that the unit was ordered on.                                                                                                                                                                                          |
| PeriodType                        | This field displays the Warranty Period of the unit.                                                                                                                                                                                                      |
| POBranch                          | This field displays the Branch that issued the Sales Purchase Order for the Unit.                                                                                                                                                                         |
| PODealCustomer                    | This field displays the Customer Number tied to the Deal when the Deal number is referenced to a Sales Purchase Order.                                                                                                                                    |
| PODealCustomerName                | This field displays the Customer Name tied to the Deal when the Deal number is referenced to a Sales Purchase Order.                                                                                                                                      |
| PODepartment                      | This field displays the Sales Department responsible for issuing the Sales Purchase Order.                                                                                                                                                                |
| PONumber                          | This field displays the customer's PO number.                                                                                                                                                                                                             |
| PreviousOwner                     | This field displays the previous owner of a unit.                                                                                                                                                                                                         |
| ProductClass                      | This field displays the product class associated with a given lease/rental charge.                                                                                                                                                                        |
| PurchaseCost                      | This field displays the amount for which a unit was purchased. Updates from the manufacture's received invoice.                                                                                                                                           |
| PurchaseOrderStatus               | This field displays the status of a customer's PO.                                                                                                                                                                                                        |
| ReceiveInvoiceDate                | This field displays the date on which a unit was received.                                                                                                                                                                                                |
| ReceiveInvoiceNumber              | This field displays the received manufactuer's invoice number.                                                                                                                                                                                            |
| ReceivedDate                      | This field displays the date on which a purchase order was received.                                                                                                                                                                                      |
| ReplenishStock                    | This flag is used to denote whether the unit was purchased to Replenish Stock or not.                                                                                                                                                                     |
| RequestShipDate                   | This field displays the date on which shipment of a unit has been requested.                                                                                                                                                                              |
| SellingStatus                     | This field displays the unit's selling status (Available, Deal Contract, Sold, etc.).                                                                                                                                                                     |
| SoldCustomerName                  | This field displays the Customer Name of the Customer that the Unit was sold to.                                                                                                                                                                          |
| SoldCost                          | This field displays the Cost of the unit at the time the Unit was sold.                                                                                                                                                                                   |
| SoldCustomerKey                   | This field displays the Customer Number of the Customer that the Unit was sold to.                                                                                                                                                                        |
| SoldCustomerAddress1              | This field displays Address Line 1 of the Customer that the Unit was sold to.                                                                                                                                                                             |
| SoldCustomerAddress2              | This field displays Address Line 2 of the Customer that the Unit was sold to.                                                                                                                                                                             |
| SoldCustomerCity                  | This field displays the City of the Customer that the Unit was sold to.                                                                                                                                                                                   |
| SoldCustomerCountry               | This field displays the Country of the Customer that the Unit was sold to.                                                                                                                                                                                |
| SoldCustomerCounty                | This field displays the County of the Customer that the Unit was sold to.                                                                                                                                                                                 |
| SoldCustomerPostalCode            | This field displays the Postal Code of the Customer that the Unit was sold to.                                                                                                                                                                            |
| SoldCustomerRegion                | This field displays the Region (State or Province) of the Customer that the Unit was sold to.                                                                                                                                                             |
| SoldDate                          | This field displays the date on which a core was sold.                                                                                                                                                                                                    |
| SoldInvoiceNumber                 | This field displays the Invoice Number that the Unit was sold on.                                                                                                                                                                                         |
| SoldPrice                         | This field displays the Price of the unit at thte time the Unit was sold.                                                                                                                                                                                 |
| SoldSalesperson                   | This field displays the Salesperson responsible for the Sale of the unit.                                                                                                                                                                                 |
| SpecialPrice                      | This field displays the asking price, expressed in dollars, listed for a unit for a limited time.                                                                                                                                                         |
| SpecialPriceExpiration            | This field displays the date a special price offered on a unit expires.                                                                                                                                                                                   |
| StockNumber                       | This field displays the stock number attached to a unit.                                                                                                                                                                                                  |
| TemporaryLocationName             | This field displays the Name of the Temporary location if one is associated with the unit.                                                                                                                                                                |
| TemporaryLocationType             | This field displays the Temporary Location Type (Branch, Vendor or Customer) if one is associated with the unit.                                                                                                                                          |
| TireTaxCredit                     | This field displays the tire tax credit FET exempt amount assigned to the give unit.  This amount comes from the value assigned to the unit in the unit file.  If the amount for the unit is overwritten on a deal, it will not be reflected here.        |
| TitleRegion                       | This field displays the Region (State or Province) the Title was issued from for the Unit.                                                                                                                                                                |
| TotalUnitCost                     | This field displays the sum of Base Cost, Current Cost, and Open LPOs.                                                                                                                                                                                    |
| TradeInAllowance                  | This field displays the amount, in dollars for which is offered on a trade-in unit.                                                                                                                                                                       |
| UnitCostConversion                | This field displays the value used to control when the cost of the unit is converted from the foreign currency to the local currency (i.e., during receive invoice, when the unit is added to the quote, during invoicing, or when accounting is posted). |
| UnitCostConverted                 | This field denotes whether Cost of the Unit has been converted using Currency Exchange.                                                                                                                                                                   |
| UnitIndicator                     | This field displays the unit indicator of the given unit.                                                                                                                                                                                                 |
| UnitNumber                        | This field displays the ID number of a unit attached to a given note.                                                                                                                                                                                     |
| UsageType                         | This field displays the Usage Type of the Unit if they have been established and assigned to the unit.                                                                                                                                                    |
| VIN                               | This field displays the Vehicle Identification Number.                                                                                                                                                                                                    |
| VoidOrderDate                     | This field displays the Void Order Date of the Sales Purchase Order if it has been Voided.                                                                                                                                                                |
| WarrantyContract                  | This field displays the Warranty Contract information for the unit.                                                                                                                                                                                       |
| WarrantyMeter                     | This field displays the Meter Reading for the Unit's Warranty.                                                                                                                                                                                            |
| WarrantyPeriod                    | This field displays the Warranty Period for the Unit's Warranty.                                                                                                                                                                                          |
| Year                              | This field displays the model year of the unit.                                                                                                                                                                                                           |

---
---
### Components
---

This data object is used to display all Unit Component information for a given
unit.  By default, both Active and Inactive Unit Occurrences that contain
Component information are returned.

This information can be found on the Component tab of Unit Maintenance within
the Fusion Business System. 

<!-- 


  -->  <hr>Field Details...

| **SQL Field Name**      | **Column Description**                                                                                            |
|---|---|
| IsActiveUnit            | This displays whether or not the given unit number is the active occurence for the unit.                          |
| AddDate                 | This field displays the user that added the component.                                                            |
| AddUser                 | This field displays the date that the component was added.                                                        |
| ComponentDeactivateDate | This field displays the De-activation date of the component.                                                      |
| ComponentManufacturer   | This field displays the manufacturer of the component.                                                            |
| ComponentModel          | This field displays the model of the component.                                                                   |
| ComponentName           | This field displays the name of the component.                                                                    |
| Description             | This field displays the Description of the Component.                                                             |
| CurrentMeterReading     | This field displays the current meter reading for the unit.                                                       |
| CurrentMeterReadingDate | This field displays the date associated with the current meter reading.                                           |
| Deductible              | This field contains the dollar amount that must be met before the warranty is in effect.                          |
| InServiceDate           | This field displays the in service date of the unit.                                                              |
| LastUpdate              | This field displays the date that the component was updated.                                                      |
| UpdateUser              | This field displays the user that last updated the component.                                                     |
| MeterType               | This displays the meter type of the component.                                                                    |
| PartNumber              | This field displays the part number of the component (if applicable).                                             |
| SerialNumber            | This field displays the serial number of the component.                                                           |
| UnitIndicator           | This field displays the Unit Indicator of the unit the component is associated with.                              |
| UnitNumber              | This field displays the Unit number the component is attached to.                                                 |
| WarrantyContract        | This field displays the document number identifying the warranty agreement between the manufacturer and customer. |
| WarrantyLaborPercentage | This field displays the percentage of labor that is covered by warranty.                                          |
| WarrantyMeter           | This field should contain the number of miles for which the unit is under warranty.                               |
| WarrantyPartPercentage  | This field displays the percentage of parts that are covered by the warranty.                                     |
| WarrantyPeriod          | This field contains the time that the component is covered under warranty.                                        |
| WarrantyPeriodType      | This field defines what the warranty period is for the unit.                                                      |

---
---
### Owning Customer
---

This data object is used to display the owning customer(s) of all Service units.
In the case of units with dual ownership, a record will be returned for each
customer corresponding to that unit.

This information comes from the Service tab in the Unit application in Fusion,
and for units with dual ownership, the Service Unit Customer Maintenance
application, which can be opened by clicking the Service Unit Customer Legacy
Links hyperlink on the Service tab.

<!-- 


  -->  <hr>Field Details...

| **SQL Field Name**        | **Column Description**                                                                                           |
|---|---|
| AddDate                   | This field displays the date on which the given owning customer was added to the given unit.                     |
| AddUser                   | This field displays the username of the user who added the given owning customer to the given unit.              |
| CharacteristicType        | This field displays the characteristic type of the given unit.                                                   |
| CompanyName               | This field displays the company name of the given owning customer of the given unit.                             |
| CustomerBaseBranch        | This field displays the base branch associated with the given owning customer of the given unit.                 |
| CustomerNumber            | This field displays the customer number of the given owning customer of the given unit.                          |
| Inactive                  | This field displays whether the given unit is marked as inactive in Fusion.                                      |
| IndustryType              | This field displays the industry type of the given owning customer of the given unit.                            |
| LastUpdateDate            | This field displays the date on which the given owning customer was last updated on the given unit.              |
| LastUpdateUser            | This field displays the username of the user who last updated the given owning customer on the given unit.       |
| Make                      | This field displays the make of the given unit.                                                                  |
| Manufacturer              | This field displays the manufacturer of the given unit.                                                          |
| Model                     | This field displays the model of the given unit.                                                                 |
| OutsidePartsSalesperson   | This field displays the outside parts salesperson associated with the given owning customer of the given unit.   |
| OutsideServiceSalesperson | This field displays the outside service salesperson associated with the given owning customer of the given unit. |
| UnitNumber                | This field displays the unit number of the given unit that is owned by the given customer.                       |
| VIN                       | This field displays the vehicle identification number of the given unit.                                         |
| Year                      | This field displays the model year of the given unit.                                                            |

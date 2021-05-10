---
layout: post
title: "Parts Supplier"
category: "Parts" 
icon: "icon-gear"
type: "data_access" 
comments: false
description: Access all suppliers that are set up within the Fusion business system
---

---
---

This data object is used to show all suppliers that are set up within the Fusion business system.

This information can be found within the Supplier record in the Fusion business system.

 
#### URL 
```
/frw/Supplier
``` 
 <hr>
Field Details...

| **SQL Field Name**            | **Column Description**                                                                                                                                                                                                                                   |
|---|---|
| AccountingGroup | This field displays the accounting group field of the given supplier that will populate in a new part record. | 
| AddDate | This field displays the date on which the given supplier was added in the Business System. | 
| AddUser | This field displays the user name that added the record. | 
| Address1 | This field displays the primary address line 1 of the supplier. | 
| Address2 | This field displays the primary address line 2 of the supplier. | 
| AlternateSupplier | This field displays the partent supplier for the given supplier. | 
| APVendor | This field displays the A/P vendor. | 
| CompanyName | This field displays the company name of an A/P vendor associated with the supplier. | 
| BarCodeMultiplier | This field displays the multipler used when scanning parts in during bar code receiving of the given supplier that will populate in a new part record. | 
| BuyTime | This field displays the buy time field of the given supplier that will populate in a new part record. | 
| CellPhone | This field displays the primary cell phone of the supplier. | 
| CharacteristicType | This field will display the Characteristic Type that will be used as a default for all parts created for the specific supplier. | 
| City | This field displays the primary city of the supplier. | 
| Code1 | This field displays the Code 1 field of the given supplier that will populate in a new part record. | 
| Code2 | This field displays the Code 2 field of the given supplier that will populate in a new part record. | 
| Code3 | This field displays the Code 3 field of the given supplier that will populate in a new part record. | 
| Code4 | This field displays the Code 4 field of the given supplier that will populate in a new part record. | 
| Code5 | This field displays the Code 5 field of the given supplier that will populate in a new part record. | 
| CoreRightToReturnDaysCustomer | This field displays the number of days before the right to return to vendor expires. | 
| CoreRightToReturnDaysSupplier | This field displays the number of days a customer has to return a core before the right to return expires. | 
| Country | This field displays the primary country of the supplier. | 
| County | This field displays the primary county of the supplier. | 
| CurrencyCode | This field displays the currency code  of the given supplier that will populate in a new part record. | 
| CurrencyExchangeBroker | This field displays the currency exchange broker field of the given supplier that will populate in a new part record. | 
| DaysOfStock | This field displays the number of days of stock that should be carried in inventory. | 
| DutyCode | This field displays the duty rate of the given supplier that will populate in a new part record. | 
| E-MailAddress | This field displays the primary E-mail of the supplier. | 
| Fax | This field displays the primary fax number of the supplier. | 
| FirstName | This field displays the first name of the primary contact of the supplier. | 
| ImportFreightMultiplier | This field displays the freight multiplier of the given supplier that will populate in a new part record. | 
| Inactive | This field displays whether or not a given supplier record is set to inactive. | 
| LastName | This field displays the last name of the primary contact of the supplier. | 
| LastOrderDate | This field displays the date on which a part was last ordered. | 
| LastUpdateDate | This field displays the last updated of the given supplier. | 
| LastUpdateUser | This field displays the user who last updated the given supplier. | 
| LeadTime | This field displays the number of days between placing an order until receiving an order. | 
| ListMultiplier | This field displays the multipler associated with list price of the given supplier that will populate in a new part record. | 
| ManufacturerCode | This field displays the manufacturerer code of the given supplier that will populate in a new part record. | 
| MinimumOrderDollar | This field displays the minimum order, expressed in dollars, required by a supplier. | 
| MaximumOrderWeight | This field displays the maximum order weight for a supplier. | 
| MinimumReturnDollar | This field displays the minimum order, expressed in dollars, required by a supplier for return orders. | 
| MinimumReturnWeight | This field displays the minimum weight, required by a supplier for return orders. | 
| OEMBreakdown | This field identifies if the given supplier is purchased from an OEM. | 
| IsOEMBreakdownPrinted | This field identifies the default value for the given supplier will have additional classification on some reports that will populate in a new part record. | 
| OfficePhone | This field displays the primary office phone of the supplier. | 
| OrderFrequency | This field displays how often you place an order (once a week, daily, etc.). | 
| OrderGroup | This field displays the order group attached to the supplier. | 
| PostalCode | This field displays the primary postal code of the supplier. | 
| Price1Multiplier | This field displays the price 1 multiplier of the given supplier that will populate in a new part record. | 
| Price2Multiplier | This field displays the price 2 multiplier of the given supplier that will populate in a new part record. | 
| Price3Multiplier | This field displays the price 3 multiplier of the given supplier that will populate in a new part record. | 
| Price4Multiplier | This field displays the price 4 multiplier of the given supplier that will populate in a new part record. | 
| Price5Multiplier | This field displays the price 5 multiplier of the given supplier that will populate in a new part record. | 
| Price6Multiplier | This field displays the price 6 multiplier of the given supplier that will populate in a new part record. | 
| Price7Multiplier | This field displays the price 7 multiplier of the given supplier that will populate in a new part record. | 
| PriceFileSource | This field identifies the price file associated with the given supplier that will populate in a new part record. | 
| PriceGroup | This field identifies the price group associated with the given supllier that will populate in a new part record. Used to group like parts together for customer special pricing. | 
| ProductClass | This field displays the product class  of the given supplier that will populate in a new part record. | 
| PurchaseMethod | This field displays the default purchase method of the given supplier that will be populated on a new part record for the supplier. | 
| Region | This field displays the primary region of the supplier. | 
| ReplacementCostMultiplier | This field displays the default  replacement cost multiplier of the given supplier that will be populated on a new part record for the supplier. | 
| IsRequireStockClass | This field will determine whether or not parts being created or edited in the selected supplier will require the user to populate the Stock Class field on the Parts Inventory record. | 
| IsRestrictedSupplier | This field displays the value of the restricted supplier checkbox of the given suppler. This will determine whether or not the parts within the supplier are able to have pricing maintained in Point of Sale and Pricing programs in Fusion. | 
| SafetyStockPercent | This field displays the default safety stock percent of the give supplier, which is a percentage between 0 and 100 that an order point will be padded. This field fill be populated with this amount when a new part record is created for the supplier. | 
| Salutation | This field displays the salutation of the primary contact of the supplier. | 
| Seasonal | This field displays whether or not a part is seasonal (80% of sales of a given part occur in six consecutive months or less). | 
| ShopPhone | This field displays the primary shop phone of the supplier. | 
| StockClass | This field displays a subset within a supplier, typically used in pricing and typically provided by the manufacturer. | 
| SuggestedOrderMonths | This field displays the number of months of sales history to consider when determining purchase orders for a supplier. | 
| SupplierCode | This field displays the code attached to a supplier for a part. | 
| NAME | This field displays the name of the supplier. | 
| Title | This field displays the title of the primary contact of the supplier. | 
| UnitOfMeasure | This field deipslays the default unit of measure for the given supplier and is populated on new part records. | 
| UpdateFromPriceFile | This field displays the default value for the given supplier. This will determine whether or not a part number is updated from the price file- if unchecked, users manually control pricing on new part records. | 
| WebAddress | This field displays the primary web address of the supplier. | 



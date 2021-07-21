---
layout: post
title: "Parts Inventory Extended"
category: "Parts" 
icon: "icon-gear"
type: "data_access" 
comments: false
description:  Access to physical inventory extended detail information within Fusion
---

---
---

 
#### URL 
```
/frw/PartsInventoryExtended
``` 
 <hr>
Field Details...

 | Name | Type | Description |
 | --- | --- | --- |
 | PartsInventoryDetailID | int | ID of the Part Inventory Detail | 
 | PartNumber | varchar(50) | This field displays the part number of the given part. | 
 | SupplierCode | varchar(20) | Supplier Code | 
 | SupplierID | int | Supplier DB ID | 
 | Description | varchar(50) | This field displays the description associated with the given part. | 
 | PartType | varchar(20) | This field displays whether the given part is a part, exchange, or core. | 
 | CorePartsInventoryID | int | ID of the Core Part Inventory | 
 | PartsInventoryID | int | ID of the Part Inventory | 
 | BranchCode | varchar(10) | Branch Code | 
 | BranchID | int | Branch ID in Fusion | 
 | QuantityAvailable | int | This field displays the quantity of the given part available to be sold. | 
 | AverageCost | decimal | This field displays the average cost of the given part or, if average cost is zero, displays the replacement cost of that part. | 
 | CurrentMonthUsage | int | Current Month Usage | 
 | CurrentMonthPicks | int | Current Month Picks | 
 | CurMonthSales | int | This field displays the number of sales for the given part in the current month. | 
 | CurMonthManualSales | int | This field displays the number of manually entered sales for the given part in the current month. | 
 | CurMonthTotalSales | int | This field displays the total of sales (automatic and manual) for the given part in the current month. | 
 | CurMonthPicks | int | This field displays the number of picks for the given part in the current month. | 
 | CurMonthManualPicks | int | This field displays the number of manually entered picks for the given part in the current month. | 
 | CurMonthTotalPicks | int | This field displays the total of picks (automatic and manual) for the given part in the current month. | 
 | CurMonthTotalLostSales | int | This field displays the total of lost sales for the given part in the current month. | 
 | CurYearSales | int | This field displays the number of sales for the given part in the current year. | 
 | CurYearManualSales | int | This field displays the number of manually entered sales for the given part in the current year. | 
 | CurYearTotalSales | int | This field displays the total of sales (automatic and manual) for the given part in the current year. | 
 | CurYearPicks | int | This field displays the number of picks for the given part in the current year. | 
 | CurYearManualPicks | int | This field displays the number of manually entered picks for the given part in the current year. | 
 | CurYearTotalPicks | int | This field displays the total of picks (automatic and manual) for the given part in the current year. | 
 | CurYearTotalLostSales | int | This field displays the total of lost sales for the given part in the current year. | 
 | PriorYearSales | int | This field displays the number of sales for the given part in the prior year. | 
 | PriorYearManualSales | int | This field displays the number of manually entered sales for the given part in the prior year. | 
 | PriorYearTotalSales | int | This field displays the total of sales (automatic and manual) for the given part in the prior year. | 
 | PriorYearPicks | int | This field displays the number of picks for the given part in the prior year. | 
 | PriorYearManualPicks | int | This field displays the number of manually entered picks for the given part in the prior year. | 
 | PriorYearTotalPicks | int | This field displays the total of picks (automatic and manual) for the given part in the prior year. | 
 | PriorYearTotalLostSales | int | This field displays the total of lost sales for the given part in the prior year. | 
 | 13MonthSales | int | This field displays the number of sales for the given part in the current month plus the preceding 12 months. | 
 | 13MonthManualSales | int | This field displays the number of manually entered sales for the given part in the current month plus the preceding 12 months. | 
 | 13MonthTotalSales | int | This field displays the total of sales (automatic and manual) for the given part in the current month plus the preceding 12 months. | 
 | 13MonthPicks | int | This field displays the number of picks for the given part in the current month plus the preceding 12 months. | 
 | 13MonthManualPicks | int | This field displays the number of manually entered picks for the given part in the current month plus the preceding 12 months. | 
 | 13MonthTotalPicks | int | This field displays the total of picks (automatic and manual) for the given part in the current month plus the preceding 12 months. | 
 | 13MonthTotalLostSales | int | This field displays the total of lost sales for the given part in the current month plus the preceding 12 months. | 
 | AddUserID | int |  | 
 | UpdateUserID | int |  | 
 | CorePartsInventoryDetailID | int |  | 
 | InherentCoreAverageCost | decimal | This field displays the inherent core average cost of the core associated with the given part or, if the inherent core average cost is zero, displays the replacement cost of the core. | 
 | BinLocation | varchar(20) | This field displays the bin location where the given part is stored. | 
 | LastReceivedDate | datetime | This field displays the date on which the given part was last received into inventory. | 
 | LastAveragingQuantity | int | This field displays the quantity of the given part that the latest average cost was based on. | 
 | Inactive | bit | This field displays whether the given part record has been set to inactive. | 
 | LastSoldDate | datetime | This field displays the date on which the given part was last sold (present on a parts order or a repair order at the time of invoicing). | 
 | LastCountDate | datetime |  | 
 | StockStatusID | int |  | 
 | BarCode | varchar(50) | This field displays the bar code associated with the given part. | 
 | StockClass | varchar(10) | This field displays the stock class of the given part. | 
 | Code1 | varchar(10) | This field displays the code 1 associated with the given part. | 
 | Code2 | varchar(10) | This field displays the code 2 associated with the given part. | 
 | Code3 | varchar(10) | This field displays the code 3 associated with the given part. | 
 | Code4 | varchar(10) | This field displays the code 4 associated with the given part. | 
 | Code5 | varchar(10) | This field displays the code 5 associated with the given part. | 
 | UpdateFromPriceFile | bit | This field displays whether the pricing of the given part is updated via price file. | 
 | TrackAvailabilityQuantity | bit |  | 
 | AlternateSupplierID | int |  | 
 | InventoryClass | varchar(10) | This field displays the inventory class in which the given part is categorized. | 
 | VelocityCode | varchar(10) | This field displays the velocity code associated with the given part. | 
 | ReturnCode | varchar(10) | This field displays the return code associated with the given part. | 
 | QL_PriceGroupID | int |  | 
 | PriceGroup | varchar(50) | This field displays the price group that the given part is associated with. | 
 | SellPackage | int | This field displays the package size in which the given part is sold to customers. | 
 | PriceFileFactor | int | This field displays the divisor to be used to convert the unit of measure from the price file for the given part to the resale unit of measure for the given part. | 
 | Price1 | decimal | This field displays the level 1, or highest, price for the given part. | 
 | Price2 | decimal | This field displays the level 2 price for the given part. | 
 | Price3 | decimal | This field displays the level 3 price for the given part. | 
 | Price4 | decimal | This field displays the level 4 price for the given part. | 
 | Price5 | decimal | This field displays the level 5 price for the given part. | 
 | Price6 | decimal | This field displays the level 6 price for the given part. | 
 | Price7 | decimal | This field displays the level 7, or lowest, price for the given part. | 
 | ListPrice | decimal | This field displays the list price of the given part, either from the manufacturer or entered by the user. | 
 | PurchaseMethodID | int |  | 
 | SafetyStockPercent | int | This field displays the percentage that the order point should be padded with when determining whether to restock the given part. | 
 | JobQuantity | int | This field displays the minimum quantity of the given part needed to complete one service job. | 
 | Seasonal | bit |  | 
 | OrderPoint | int | This field displays the order point for the given part, as indicated on the purchase control tab in the part record. | 
 | FreezeDate | datetime | This field displays the date through which the line point, order point, and order quantity calculations should be frozen. | 
 | MinimumQuantity | int | This field displays, for parts with a purchase method of min/max, the minimum quantity at which the given part will be restocked. | 
 | MaximumQuantity | int | This field displays, for parts with a purchase method of min/max, the maximum quantity that the given part will be restocked to when it reaches the minimum quantity. | 
 | LeadTime | int | This field displays the number of days that will pass between placing an order and receiving an order for the given part. | 
 | OrderFrequency | int | This field displays at what frequency orders are, or can be, placed for the given part. | 
 | DaysOfStock | int | This field displays the number of days of stock that should be in inventory for the given part, from the purchase control tab in the part record. | 
 | BuyTime | int | This field displays the buy time of the given part from the purchase control tab on the part record. | 
 | AverageLeadTime | int | This field displays the average lead time for the given part from the purchase control tab on the part record. | 
 | DaysOutMTD | int | This field displays the number of days during the current month that the given part has been out of stock, from the purchase control tab in the part record. | 
 | BuyPackage | int | This field displays the buy package size for the given part from the purchase control tab on the part record. | 
 | PurchaseConversion | int | This field displays the multiplier to be used to convert the selling unit of measure to the purchasing unit of measure from the vendor for the given part. | 
 | SupplierBuyPackage | int | This field displays the quantity in which the given part is purchased from the supplier. | 
 | QL_PurchaseUnitOfMeasureID | int |  | 
 | PurchUnitofMeasure | varchar(50) |  | 
 | DateAdded | datetime | This field displays the date on which the given part record was added to inventory, from the purchase control tab in the part record (this date can be manually updated, so could differ from Add Date). | 
 | LastReplacementCostChangeDate | datetime | This field displays the date on which the replacement cost of the given part was last changed. | 
 | LastPriceChangeDate | datetime | This field displays the date on which the price of the given part was last changed. | 
 | LastPriceFileUpdate | datetime | This field displays the date on which the price file for the given part was last updated. | 
 | LastOrderedDate | datetime | This field displays the date on which the given part was last ordered. | 
 | LastOutOfStockDateGMT | datetime |  | 
 | LastPuchaseCost | decimal |  | 
 | QuantityCommitted | int | This field displays the quantity of the given part that has been added to open parts or repair orders. | 
 | QuantityOnOrder | int | This field displays the quantity of the given part that has been ordered from vendors, but is not available in inventory yet. | 
 | QuantityOnBackOrder | int | This field displays the quantity of the given part that has been ordered by a customer but is not currently available in inventory. | 
 | ReplacementCost | decimal | This field displays the replacement cost of the given part. | 
 | QL_SellingUnitOfMeasureID | int |  | 
 | SellingUnitOfMeasure | varchar(50) | This field displays the unit of measure in which the given part is sold to the customer. | 
 | Weight | decimal | This field displays the weight of the given part. | 
 | ProductClassID | int |  | 
 | BinLocationID | int |  | 
 | ExcludeFromCostMatrix | bit | This field displays whether the given part is excluded from cost matrix pricing. | 
 | PriceFileSourceID | int |  | 
 | PriceFilePartNumber | varchar(50) | This field displays the part number from the manufacturer on the price file for the given part, if it differs from the part number of the part in Fusion. | 
 | IsPriceUpdatedDuringReceiving | bit |  | 
 | SupersedePriceFilePartNumber | varchar(50) | This field displays the part number in the price file that the given part has superseded to. | 
 | SerialNumber | varchar(20) |  | 
 | EHCCodeID | int |  | 
 | EHCCode | varchar(10) | This field displays the name of the environmental handling charge to be charged when the given part is purchased. | 
 | AccountingGroupID | int |  | 
 | AccountingGroup | varchar(10) | This field displays the accounting group to which the given part belongs. | 
 | ExcludeFromVelocityPricing | bit | This field displays whether the given part is excluded from velocity pricing. | 
 | ExcludeFromPriceRounding | bit | This field displays whether the given part is excluded from price rounding. | 
 | CurrencyExchangeCodeID | int |  | 
 | CurrencyCode | varchar(10) | This field displays the currency code associated with the given part. | 
 | CurrencyExchangeDutyCodeID | int |  | 
 | DutyCode | varchar(50) | This field displays the duty code to be used if the given part is purchased in another currency. | 
 | CurrencyExchangeBrokerID | int |  | 
 | CurrencyExchangeBroker | varchar(50) |  | 
 | ImportFreightMultiplier | decimal | This field displays the freight multiplier to be used if the given part was purchased in another currency. | 
 | ExcludeFromCurrencyExchange | bit | This field displays whether the given part is excluded from currency exchange. | 
 | ImportCost | decimal | This field displays the cost at which the given part was imported into the country. | 
 | SerialStockTypeID | int | ID of the Serial Stock Type | 
 | IsRecommendedStockingPartFreightLiner | bit |  | 
 | IsMissionCriticalPartFreightLiner | bit |  | 
 | IsFleetStockingPartFreight | bit |  | 
 | FullBinQuantity | int | This field displays the quantity of the given part in a full bin, as indicated on the OEM control tab. | 
 | StockStatus | varchar(50) | This field displays the stock status of the given part. | 
 | AlternateSupplier | varchar(20) | This field displays the alternate supplier, if one exists, for the given part. | 
 | OverrideProductClass | varchar(50) | This field displays the override product class, if one exists, for the given part. | 
 | PurchaseMethod | varchar(20) | This field displays the purchase method associated with the given part, which determines at what point the part will be restocked. | 
 | BarCodeMultiplier | varchar(25) | This field displays the bar code multiplier for the given part from the purchase control tab on the part record. | 
 | PriceFileSource | varchar(20) | This field displays the name of the price file for the given part. | 
 | PriceFileSourceDescription | varchar(50) | This field displays a description of the price file for the given part. | 
 | SerialStockType | varchar(50) | This field displays whether a serial number is required for the given part (No indicates that it is not required, Point of Sale indicates that it will be required at the point of sale). | 
 | KitType | varchar(10) | This field displays whether the given part has a kit type of kit, assembly, or part. | 
 | CorePartNumber | varchar(50) | This field displays the part number of the core associated with the given part. | 
 | CoreSupplier | varchar(20) | This field displays the supplier of the core associated with the given part. | 
 | CoreDescription | varchar(50) | This field displays the description of the core associated with the given part. | 
 | CoreReplacementCost | decimal | This field displays the replacement cost of the core associated with the given part. | 
 | CoreAverageCost | decimal | This field displays the average cost of the core associated with the given part or, if average cost of the core is zero, displays the replacement cost of the core. | 
 | CorePrice1 | decimal | This field displays the price 1 of the core associated with the given part. | 
 | CorePrice2 | decimal | This field displays the price 2 of the core associated with the given part. | 
 | CorePrice3 | decimal | This field displays the price 3 of the core associated with the given part. | 
 | CorePrice4 | decimal | This field displays the price 4 of the core associated with the given part. | 
 | CorePrice5 | decimal | This field displays the price 5 of the core associated with the given part. | 
 | CorePrice6 | decimal | This field displays the price 6 of the core associated with the given part. | 
 | CorePrice7 | decimal | This field displays the price 7 of the core associated with the given part. | 
 | CoreListPrice | decimal | This field displays the list price of the core associated with the given part. | 
 | LifoCost | decimal | This field displays the current LIFO cost of the given part. | 
 | LifoDate | datetime | This field displays the date on which the current LIFO cost of the given part was recorded. | 
 | LastLifoCost | decimal | This field displays the last LIFO cost of the given part. | 
 | LastLifoDate | datetime | This field displays the date on which the last LIFO cost of the given part was recorded. | 
 | CountryOfOrigin | varchar(50) | This field displays the country from which the given part originates. | 
 | AlternateDescription | varchar(100) | This field displays the alternate description, if one exists, for the given part from the inventory control tab on the part record. | 
 | TariffNumber | varchar(50) | This field displays the tariff number associated with the given part. | 
 | ProductCharacteristic | varchar(50) | This field displays additional information about the given part number, intended to supplement the Alternate Description field. | 
 | IsPrintLabel | bit | This field displays whether an option will be available to print a label for the given part when it is added to a parts order. | 
 | IsInventory | int |  | 
 | AddDate | datetime | This field displays the date on which the given parts inventory record was added to Fusion (this is a system generated field, which is displayed at the bottom of the Parts Inventory application). | 
 | AddUser | varchar(20) | This field displays the username of the user who added the given parts inventory record to Fusion. | 
 | LastUpdateDate | datetime | This field displays the date on which the given parts inventory record was last updated in Fusion. | 
 | LastUpdateUser | varchar(20) | This field displays the username of the user who last updated the given parts inventory record in Fusion. | 
 | IsMDIControlled | bit | This field displays whether the given parts inventory record is controlled by MDI, as indicated on the OEM Control tab in the Parts Inventory application. | 
 | AlternateBin | nvarchar(max) | This field displays a list of all Alternate Bins that are associated with the given part record.  The alternate bin locations returned in the list are seperated by a comma. | 
 | ExcludefromPartsASIST | bit | Controls whether parts will be excluded when gathering data for Mack/Volvo PartsASIST messages. | 
 | BrandID | varchar(1) | Reporting field used by Mack/Volvo to determine the part’s price file origin. | 
 | System | nvarchar(256) | The 3 digit number identifying the system involved, e.g., brakes. | 
 | Assembly | nvarchar(256) | The 3 digit number that identifies the part; this is a generic term for the part that differs from the manufacturer part number, e.g., front brake lining. | 
 | Component | nvarchar(256) | The 3 digit number used to further identify the System, e.g., front brakes. | 
 | CharacteristicType | varchar(20) | This field displays the Characteristic Type that is associated with a Master Parts Inventory Record. The Characteristic Types are setup INV91110 Parts Inventory Characteristic Type and controls which characteristics can be tracked for specific parts. | 
 | SerializedStockQuantityAvailable | int | This field represents the total quantity of active and available Serial Numbered records that for the specific Branch Part Number.  This data can be found in INV91160 Parts Inventory Serialized Stock or in the Parts Inventory record itself. | 
 | SupplementalPriceFilePartNumber | varchar(50) | This field displays the Price File Part Number field in the Supplemental Price File Group Box on the Parts Inventory Record. | 
 | SupplementalPriceFileSource | varchar(20) | This field displays the name of the Price File Source field in the Supplemental Price File Group Box on the Parts Inventory Record. | 
 | SupplementalPriceFileSourceDescription | varchar(50) | This field displays the description of the Price File Source in the Supplemental Price File Group Box on the Parts Inventory Record. | 
 | PriceBreakCost | decimal | This field represents the cost of the part that the user can order it at when placing a purchase order for a specific quantity. This quantity is usually a larger or package quantity so the cost is lower for ordering in bulk. | 
 | PriceBreakQuantity | int | This field represents the quantity of the part that the user should order to receive the Price Break Cost when purchasing parts from a vendor. | 
 | SerializedStockExtendedReplacementCost | decimal | This field represents the sum of the Replacement Cost of all active and available Serial Numbered records that for the specific Branch Part Number. This data can be found in INV91160 Parts Inventory Serialized Stock or in the Parts Inventory record itself. | 
 | PriceBreakCostMultiplier | decimal | This field represents the multiplier that can be applied against the Price Break Cost field that can be pulled from a Price File when updating the Price Break Cost of a Part from a Price File field in Price File Processing. | 
 | PriceBreakExpirationDate | datetime | This field represents the expiration date of Price Break Cost of the Part Number. | 
 | ExcessQuantityAvailable | int | This field will display the amount of excess quantity available of the part.  Excess Quantity Available is any Quantity Available above the part’s Order Point if it is a Buy Time Purchase Method or above the part’s Maximum Quantity if it is a Min/Max Purchase Method and the Stock Status is “Stock”.  If the Part is not a Stock Status of “Stock” then any quantity available is considered excess. | 

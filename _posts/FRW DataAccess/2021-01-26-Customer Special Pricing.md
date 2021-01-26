---
layout: post
title: "Customer Special Pricing"
category: "Parts"
icon: "icon-gear"
type: "data_access" 
comments: false
description: Access special prices for defined customers in the Fusion system.
---

---

---
#### Method GET
```
/frw/CustomerSpecialPricing
```

A GET API to Access special prices for defined customers in the Fusion system

| Field | Type |
|---|---|
|	CustomerSpecialPricingID		|		int				|
|	CustomerID						|		int				|
|	CustomerKey						|		varchar(10)		|
|	CompanyName						|		varchar(100)	|
|	QLCustomerPriceTypeID			|		int				|
|	PartsInventoryID				|		int				|
|	PartNumber						| 		varchar(50)		|
|	SupplierID						| 		int				|
|	SupplierCode					| 		varchar(20)		|
|	PartDescription					| 		varchar(50)		|
|	PartTypeID						| 		int				|
|	StockClass						| 		varchar(10)		|
|	Code1							| 		varchar(10)		|
|	Code2							| 		varchar(10)		|
|	CurrentPrice					| 		decimal			|
|	CalculatedPrice					| 		decimal			|
|	QLPriceLevelIDOfParts			| 		int				|
|	AdditionalMultiplierOfParts		| 		decimal			|
|	QLPriceLevelIDOfService			| 		int				|
|	AdditionalMultiplierOfService	| 		decimal			|
|	UsePartsPricing					| 		bit				|
|	ContractPrice					| 		decimal			|
|	ExpirationDate					| 		datetime		|
|	InternalNote					| 		varchar(100)	|
|	PricingSuppliers				| 		varchar(8000)	|
|	PricingPriceGroups				| 		varchar(8000)	|
|	AddUserID						| 		int				|
|	AddUser							| 		varchar(20)		|
|	AddDate							| 		datetime		|
|	AddDateTimeZone					| 		decimal			|
|	UpdateUserID					| 		int				|
|	UpdateUser						| 		varchar(20)		|
|	LastUpdate						| 		datetime		|
|	LastUpdateTimeZone				| 		decimal			|
|	QLCostMatrixCodeID				| 		int				|
|	AlwaysUseContractPrice			| 		bit				|
|	IsNoChargeCores					| 		bit				|
|	PartsInventoryTypeID			| 		int				|
|	VelocityCodeTypeID				| 		int				|


#### Sample Customer Special Pricing Response
```json
[
    {
        "CustomerSpecialPricingID": 1,
        "CustomerID": null,
        "CustomerKey": null,
        "CompanyName": null,
        "QLCustomerPriceTypeID": 118,
        "PartsInventoryID": null,
        "PartNumber": null,
        "SupplierID": null,
        "SupplierCode": null,
        "PartDescription": null,
        "PartTypeID": null,
        "StockClass": "",
        "Code1": "",
        "Code2": "",
        "CurrentPrice": 0.0,
        "CalculatedPrice": 0.0,
        "QLPriceLevelIDOfParts": 8,
        "AdditionalMultiplierOfParts": 0.0,
        "QLPriceLevelIDOfService": 0,
        "AdditionalMultiplierOfService": 0.0,
        "UsePartsPricing": true,
        "ContractPrice": 0.0,
        "ExpirationDate": null,
        "InternalNote": "",
        "PricingSuppliers": "",
        "PricingPriceGroups": "Promotional Products",
        "AddUserID": 42,
        "AddUser": "gwenf",
        "AddDate": "2013-03-29T22:41:10.453",
        "AddDateTimeZone": -8.0,
        "UpdateUserID": 42,
        "UpdateUser": "gwenf",
        "LastUpdate": "2013-03-29T22:41:10.453",
        "LastUpdateTimeZone": -8.0,
        "QLCostMatrixCodeID": null,
        "AlwaysUseContractPrice": false,
        "IsNoChargeCores": null,
        "PartsInventoryTypeID": null,
        "VelocityCodeTypeID": null,
        "ProcessGUID": "ef494812868dea4ab1c4edd37dd3c678"
    },
    {
        "CustomerSpecialPricingID": 2,
        "CustomerID": null,
        "CustomerKey": null,
        "CompanyName": null,
        "QLCustomerPriceTypeID": 118,
        "PartsInventoryID": null,
        "PartNumber": null,
        "SupplierID": null,
        "SupplierCode": null,
        "PartDescription": null,
        "PartTypeID": null,
        "StockClass": "",
        "Code1": "",
        "Code2": "",
        "CurrentPrice": 0.0,
        "CalculatedPrice": 0.0,
        "QLPriceLevelIDOfParts": 8,
        "AdditionalMultiplierOfParts": 1.1,
        "QLPriceLevelIDOfService": 0,
        "AdditionalMultiplierOfService": 0.0,
        "UsePartsPricing": true,
        "ContractPrice": 0.0,
        "ExpirationDate": null,
        "InternalNote": "",
        "PricingSuppliers": "",
        "PricingPriceGroups": "Air Products,Brakes and Suspension,Bus Parts,Caterpillar Engine Parts,Dealership All Makes,Dealership Proprietary Parts,Door Hardware,Emergency Lighting & Alarms,Engine Parts,Equipment,Heaters,Hitches and Utility Trailer,Landing Gear and 5th Wheels,Lift Gates,Lighting - Specialty Truck,Lighting and Electrical,Oil, Additives, Antifreeze, Freon,Paint,Parts - Miscellaneous,Placards, Signs and Flags,RV Products,Sprinter Lines,Straps and Cargo Control,Take Offs,Tanker Parts,Tire Chains,Tire Chains - Automatic,Towing Products,Trailer Hardware,Transmission and Gear,Truck Accessories,Wheels,Winches & 4 Wheel Drive Accessories",
        "AddUserID": 42,
        "AddUser": "gwenf",
        "AddDate": "2013-03-29T22:42:05.097",
        "AddDateTimeZone": -8.0,
        "UpdateUserID": 42,
        "UpdateUser": "gwenf",
        "LastUpdate": "2013-03-29T22:42:05.097",
        "LastUpdateTimeZone": -8.0,
        "QLCostMatrixCodeID": null,
        "AlwaysUseContractPrice": false,
        "IsNoChargeCores": null,
        "PartsInventoryTypeID": null,
        "VelocityCodeTypeID": null
    },
    {
        "CustomerSpecialPricingID": 3,
        "CustomerID": null,
        "CustomerKey": null,
        "CompanyName": null,
        "QLCustomerPriceTypeID": 118,
        "PartsInventoryID": null,
        "PartNumber": null,
        "SupplierID": null,
        "SupplierCode": null,
        "PartDescription": null,
        "PartTypeID": null,
        "StockClass": "",
        "Code1": "",
        "Code2": "",
        "CurrentPrice": 0.0,
        "CalculatedPrice": 0.0,
        "QLPriceLevelIDOfParts": 7,
        "AdditionalMultiplierOfParts": 0.95,
        "QLPriceLevelIDOfService": 0,
        "AdditionalMultiplierOfService": 0.0,
        "UsePartsPricing": true,
        "ContractPrice": 0.0,
        "ExpirationDate": null,
        "InternalNote": "",
        "PricingSuppliers": "",
        "PricingPriceGroups": "Snow Plows and Ice Control",
        "AddUserID": 42,
        "AddUser": "gwenf",
        "AddDate": "2013-03-29T22:43:27.06",
        "AddDateTimeZone": -8.0,
        "UpdateUserID": 42,
        "UpdateUser": "gwenf",
        "LastUpdate": "2013-03-29T22:43:27.06",
        "LastUpdateTimeZone": -8.0,
        "QLCostMatrixCodeID": null,
        "AlwaysUseContractPrice": false,
        "IsNoChargeCores": null,
        "PartsInventoryTypeID": null,
        "VelocityCodeTypeID": null
    },
    {
        "CustomerSpecialPricingID": 5,
        "CustomerID": null,
        "CustomerKey": null,
        "CompanyName": null,
        "QLCustomerPriceTypeID": 114,
        "PartsInventoryID": null,
        "PartNumber": null,
        "SupplierID": null,
        "SupplierCode": null,
        "PartDescription": null,
        "PartTypeID": null,
        "StockClass": "",
        "Code1": "",
        "Code2": "",
        "CurrentPrice": 0.0,
        "CalculatedPrice": 0.0,
        "QLPriceLevelIDOfParts": 2,
        "AdditionalMultiplierOfParts": 0.0,
        "QLPriceLevelIDOfService": 0,
        "AdditionalMultiplierOfService": 0.0,
        "UsePartsPricing": true,
        "ContractPrice": 0.0,
        "ExpirationDate": null,
        "InternalNote": "",
        "PricingSuppliers": "",
        "PricingPriceGroups": "Brakes and Suspension,Landing Gear and 5th Wheels,Lighting - Specialty Truck",
        "AddUserID": 42,
        "AddUser": "gwenf",
        "AddDate": "2013-04-02T18:40:38.72",
        "AddDateTimeZone": -8.0,
        "UpdateUserID": 42,
        "UpdateUser": "gwenf",
        "LastUpdate": "2013-04-02T18:40:38.72",
        "LastUpdateTimeZone": -8.0,
        "QLCostMatrixCodeID": null,
        "AlwaysUseContractPrice": false,
        "IsNoChargeCores": null,
        "PartsInventoryTypeID": null,
        "VelocityCodeTypeID": null
    }
]
```
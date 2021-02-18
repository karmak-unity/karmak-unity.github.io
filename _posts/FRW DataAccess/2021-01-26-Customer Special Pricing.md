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

| Field | Type | Description
|---|---|---|
|	CustomerSpecialPricingID		|		int				| ID of Customer Special Record	|
|	CustomerID						|		int				| Unique database ID of customer	|
|	CustomerKey						|		varchar(10)		| This is the Fusion Customer Number that the CSP applies to.|
|	CompanyName						|		varchar(100)	|  	Company name	|
|	QLCustomerPriceTypeID			|		int				| This is the Fusion database ID for the Customer Price Type value on the Customer Special Pricing record.  	|
|	PartsInventoryID				|		int				| Inventory database ID of the part	|
|	PartNumber						| 		varchar(50)		| part number of the given part	|
|	SupplierID						| 		int				| database Identifier of the supplier	|
|	SupplierCode					| 		varchar(20)		| supplier code of the supplier 	|
|	PartDescription					| 		varchar(50)		| description of the given parts inventory record.	|
|	PartTypeID						| 		int				| ID of the part type of the given parts inventory record.	|
|	StockClass						| 		varchar(10)		|  stock class of the given part.	|
|	Code1							| 		varchar(10)		| code 1 associated with the given part.	|
|	Code2							| 		varchar(10)		| code 2 associated with the given part.	|
|	CurrentPrice					| 		decimal			|	|
|	CalculatedPrice					| 		decimal			|	|
|	QLPriceLevelIDOfParts			| 		int				| This is the Fusion database ID for the Price Level used for the Parts Module Customer Special Pricing record	|
|	AdditionalMultiplierOfParts		| 		decimal			| This is the multiplier applied against the Price Level selected for the Parts Module Customer Special Pricing record.   	|
|	QLPriceLevelIDOfService			| 		int				| This is the Fusion database ID for the Price Level used for the Service Module Customer Special Pricing record	|
|	AdditionalMultiplierOfService	| 		decimal			| This is the multiplier applied against the Price Level selected for the Service Module Customer Special Pricing record.     	|
|	UsePartsPricing					| 		bit				| Yes or no boolean field for to use parts pricing	|
|	ContractPrice					| 		decimal			| the contracted price for the part of a given customer	|
|	ExpirationDate					| 		datetime		| expiration date of the special pricing	|
|	InternalNote					| 		varchar(100)	| This is an internal note associated with the Customer Special Pricing record.  	|
|	PricingSuppliers				| 		varchar(8000)	| This is a list of Suppliers that the Customer Special Pricing record is setup for.  	|
|	PricingPriceGroups				| 		varchar(8000)	| This is a list of Price Groups that the Customer Special Pricing record is setup for.  	|
|	AddUserID						| 		int				| ID of the user that created the CSP record	|
|	AddUser							| 		varchar(20)		| Username of the user that created the CSP record	 	|
|	AddDate							| 		datetime		| Date record was created|
|	AddDateTimeZone					| 		decimal			| Timezone record was created in	|
|	UpdateUserID					| 		int				| ID of the user that updated the CSP record	|
|	UpdateUser						| 		varchar(20)		| Username of the user that updated the CSP record	|
|	LastUpdate						| 		datetime		| Date time Record was last updated	|
|	LastUpdateTimeZone				| 		decimal			| Timezone record was last updated in	|
|	QLCostMatrixCodeID				| 		int				| This is the Fusion database ID for the Cost Matrix value on the Customer Special Pricing record.  	|
|	AlwaysUseContractPrice			| 		bit				| boolean flag for always using contract pricing	|
|	IsNoChargeCores					| 		bit				| boolean flag to determine charges around cores	|
|	PartsInventoryTypeID			| 		int				| This is the Fusion database ID for the Parts Inventory Part Type associated with the Customer Special Price Record.  	|
|	VelocityCodeTypeID				| 		int				| ID for the velocity code associated with the given part.	|

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
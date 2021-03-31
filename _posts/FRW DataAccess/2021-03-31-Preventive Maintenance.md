---
layout: post
title: "Preventive Maintenance"
category: "Repair Order"
icon: "icon-wrench"
type: "data_access" 
comments: false
description: Access all Preventive Maintenance information
---

---

This data object is used to return all Preventive Maintenance information fromt he Fusion Business System.

This information can be found in the Preventive Maintenance	application within Fusion.

 
#### URL 
```
/frw/PreventiveMaintenance
``` 
 <hr>
Field Details...

| **SQL Field Name**   | **Field Type** |
|---|---|
	|	CustomerID			|	int	|
	|	AddressID			|	int	|
	|	UnitID				|			int		|
	|	RepairOrderID		|	int		|
	|	RepairOrderTaskID	|	int	|
	|	RepairTypeID		|	int		|
	|	AddDate				|		datetime		|
	|	LastUpdate			|		datetime	|
	|	CustomerBaseBranch	|	varchar(10)	|
	|	ServiceBranch		|	varchar(10)		|
	|	CustomerNumber		|	varchar(10)		|
	|	IsLeaseRentalCustomer	|	bit		|
	|	CompanyName			|	varchar(100)		|
	|	CustomerAddress		|	varchar(100)		|
	|	CustomerCity		|	varchar(100)		|
	|	CustomerRegion		|	varchar(6)		|
	|	CustomerPostalCode	|	varchar(15)		|
	|	CustomerCountry		|	varchar(35)		|
	|	CompanyShopPhone	|	varchar(30)		|
	|	OwningCustomerContact	|	varchar(201)		|
	|	UnitNumber			|	varchar(20)		|
	|	UnitYear			|	int		|
	|	Make				|	varchar(50)		|
	|	Model				|	varchar(50)		|
	|	VIN					|	varchar(20)		|
	|	Ownership			|	varchar(1)		|
	|	PMServiceDue21Days	|	varchar(1)		|
	|	StartingMeter		|	decimal		|
	|	StartingDate		|	datetime		|
	|	AverageDailyUsage	|	int		|
	|	LastMeterDate		|	datetime		|
	|	LastMeterReading	|	decimal		|
	|	UnitType			|		varchar(20)	|
	|	LastRepairOrder		|	int	|
	|	LastInvoiceNumber	|	varchar(50)	|
	|	LastInvoiceDate		|	datetime		|
	|	PMDescription		|	varchar(50)	|
	|	GraceDays			|		int		|
	|	GraceMeter			|		decimal		|
	|	PMBasis				|		varchar(50)		|
	|	PMCode				|		varchar(20)		|
	|	PMMeterInterval		|		decimal		|
	|	PMTimeInterval		|		int		|
	|	PMRepairTypeCode		|		varchar(12)		|
	|	PMRepairTypeDescription	|		varchar(50)		|
	|	PMLastCompletionMeter	|		decimal		|
	|	PMLastCompletionDate	|		datetime		|
	|	PMDateNextDue		|		datetime		|
	|	PMNextMeterDue		|		decimal		|
	|	PMServiceDueFlag	|		varchar(1)		|
	|	PMServiceDue7Days	|		varchar(1)		|
	|	PMServiceDue14Days	|		varchar(1)		|
	|	RONumber			|		int		|
	|	ROStatus			|		varchar(20)		|
	|	RODateOpened		|		datetime		|
	|	TaskNumber			|		smallint		|
	|	TaskDescription		|		varchar(50)		|
	|	TaskClockedOnTechnicians	|		nvarchar(max)		|
	|	IsScheduled			|		bit		|
	|	LastPMROBranch		|		varchar(10)		|
	|	ContractNumber		|		int		|
	|	ContractCompanyName	|		varchar(100)		|
	|	ContractCustomerShopPhone	|		varchar(30)		|
	|	BranchID			|		int		|
	|	OpenPMROBranch			|		varchar(10)		|
	|	ContractCustomerContact	|		varchar(201)		|
	|	UnitInventoryID			|		int			|
	|	UnitIndicator			|		varchar(50)		|
	|	AddUser					|		varchar(20)		|
	|	LastUpdateUser			|		varchar(20)		|
	
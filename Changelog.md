---
layout: page
title: "Changelog"
---

---
---
## 2021-OCT
* **NEW** API Management (APIM) Portal launched. <a href="https://portal.karmak.io" target="_blank">Go To APIM portal</a>
	* All new APIs and functionality will be available within the new APIM portal.
	* Bug fixes will occur in both systems for the forseeable future. 


## 2021-SEP
* Added new fields to FRW Repair Order Header: Fusion Version of **3.62.4** or greater
* Added two new Parts Order Helpers
	* Available Payment Methods
	* Available Charge Types
* Added Payment Method ID to Create Parts Sales Order : Fusion Version of **3.62.5** or greater

## 2021-AUG
The following additions to Report Data Access require: Fusion Version of **3.62.3** or greater
* Added 2 new fields to /frw/Address


## 2021-JUL
The following require: Fusion Version of **3.62.1** or greater
* Added 11 optional fields to Create / Update Part Inventory  
* Added 2 fields to Create / Update AP vendor
* Bug fix in Price search to ensure Fusion returns contract price for customer special pricing
* Enhanced validations for Delete / Update Supersession
* AP Invoice create limits the number of characters that can be submitted for the company name to matches Fusion Logic


## 2021-JUN
* Added Get Part Supplier     (Requires Fusion Version >3.62)
* Added Get Available Branches    (Requires Fusion Version >3.62)
* Added Get Available AP Vendors    (Requires Fusion Version >3.62)
* Added Create Parts Purchase Order    (Requires Fusion Version >3.62)
* Added GET Parts Purchase Order Details    (Requires Fusion Version >3.62)
* Added GET Parts Purchase Order Search    (Requires Fusion Version >3.62)


## 2021-MAY
* Added System Status API (System Online validation)
* Updated Unit Characteristics :  update validation to ensure Characteristic value is allowed to be changed (Fusion logic validation) 

## 2021-APR
* Bug fix to ensure ProcessGUID returned with every response (including blank FRW)

## 2021-JAN
* Updated documentation for AP Invoice 
* Added Process GUID field within responses.  This is a globally unique identifier per API request.  This value should be provided to Karmak support by the API consumer in the event there are questions or issues related to the Unity system.

## 2020-DEC
* Updated documentation for Create Parts order, Users, and Parts Search

## 2020-AUG
* Added Create General Ledger : Create Journal Entry  (v.3.60.30)

## 2020-JUL
* Added Create Parts Sales Order and associated Parts search and Helper APis (v3.60.10)

## 2020-JUN
* added 'always use contract price' option to Customer special pricing  (v3.59.90)
* added documentation for View Customers (data reporting)


## 2020-MAY

#### Added Unity Workflow APIs
* AP Invoice (Create)
* AP Vendors (Create / Update)
* Part Quantity (Update)
* Technicians (Create / Update)
* Users (Create / Read / Update)cd

#### Updates
* Customers (Create / Read / Update)

## 2020-APR
### What's New
* Field aliasing capabilities for Data Access Views


## 2020-MAR
### What's New

#### Added Unity workflow APIs
* Meter Reading
* Customer Special pricing
* Quick Lists (Helper APIs)
* Parts Supersession (Create / Update / Delete)
* Parts Cross Reference (Create / Update / Delete)
* Parts Inventory (Create / Update) 
* Parts Supplier (Create / Update)

#### Added documentation for data reporting services (read only)
* Parts Inventory Receiving Detail
* Posting Reference Status (for A/P)
* Branch / Department Helper APIs
* Accounting Period (for A/P)
* Velocity Codes (Helper) for Customer Special Pricing


---
---

## 2020-JAN
### What's New

#### Added Unity workflow API Section
**Accounting**
 * Added documentation to Create Accounts Payable Invoice
 * Added documentation for Customer: Create, Update, and Retrieve

**Service**
 * Added documentation for Update Repair Type: (Activate)
 * Added documentation for Update Repair Order (add Parts)
	
**Inventory**
 * Added documentation for Update Unit Inventory
	
**Parts**
 * Added documentation for Update Part Quantity

---

#### Added Changelog :)


### Changes

**Data reporting Access**
* Reorganized Repair order to task to exist within "Repair Order" instead of "Service"

---
---

## 2019-DEC
### What's New

**Report DataAccess**


Added documentation for data reporting services (read only). The categories are:

* Accounts Payable
* Accounts Receivable
* General Ledger Accounting
* Inventory
* Lease - Rental
* Service
* Parts
* Repair Order


---
layout: post
title: "Branch Details (Helper)"
category: "Helper APIs" 
icon: "icon-question1"
type: "data_access"
comments: false
description:   Allow the user to query branch details
---

---
---


A GET API to query branch department details.

| Field | Definition | Type |
|-------------------------------|-------------------------|--------------|
| “BranchCode”                  | Branch code, or identifier for the branch.                                                                                                                                         | varchar(10)  |
| "Name"                        | Name of the branch.                                                                                                                                                                | varchar(100) |
| "Inactive"                    | When set to TRUE, this field indicates that branch record is inactive (ie, no longer used or valid for entry); inactive branches do not appear in selection lists in applications. | bit          |
| “Division”                    | Division in which the branch is grouped.                                                                                                                                           | varchar(10)  |
| “DivisionAdminBranch”         | When set to TRUE this field indicates the branch is a division administrative branch.                                                                                              | bit          |
| “CorporateAdminBranch”        | When set to TRUE, this field indicates the branch is a corporate administrative branch.                                                                                            | bit          |
| “FederalTaxID”                | Federal business registration tax identification, assigned to the branch by the federal government.                                                                                | varchar(50)  |
| “RegionTaxID”                 | Regional/state business registration tax identification, assigned to the branch by the regional government.                                                                        | varchar(50)  |
| “OfficePhone”                 | Office phone number for the branch, including dashes and spaces.                                                                                                                   | varchar(30)  |
| “ShopPhone”                   | Shop phone number for the branch, including dashes and spaces.                                                                                                                     | varchar(30)  |
| “PartsPhone”                  | Parts phone number for the branch, including dashes and spaces.                                                                                                                    | varchar(30)  |
| “Fax”                         | Fax number for the branch, including dashes and spaces.                                                                                                                            | varchar(30)  |
| “EMailAddress”                | Email address for the branch; multiple email addresses are separated with a semicolon ( ; ).                                                                                       | varchar(100) |
| “WebAddress”                  | Web address for the branch.                                                                                                                                                        | varchar(100) |
| “BillToAddress1”              | Bill-to Address - Line 1 for the branch.                                                                                                                                           | varchar(100) |
| “BillToAddress2”              | Bill-to Address - Line 2 for the branch.                                                                                                                                           | varchar(100) |
| “BillToCity”                  | Bill-to City for the branch.                                                                                                                                                       | varchar(100) |
| “BillToRegion”                | Bill-to Region for the branch.                                                                                                                                                     | varchar(6)   |
| “BillToPostalCode”            | Bill-to Postal Code for the branch.                                                                                                                                                | varchar(15)  |
| “BillToCountry”               | Bill-to Country for the branch.                                                                                                                                                    | varchar(35)  |
| “BillToCounty”                | Bill-to County for the branch.                                                                                                                                                     | varchar(34)  |
| “ShipToAddress1”              | Ship-to Address - Line 1 for the branch.                                                                                                                                           | varchar(100) |
| “ShipToAddress2”              | Ship-to Address - Line 2 for the branch.                                                                                                                                           | varchar(100) |
| “ShipToCity”                  | Ship-to City for the branch.                                                                                                                                                       | varchar(100) |
| “ShipToRegion”                | Ship-to Region for the branch.                                                                                                                                                     | varchar(6)   |
| “ShipToPostalCode”            | Ship-to Postal Code for the branch.                                                                                                                                                | varchar(6)   |
| “ShipToCountry”               | Ship-to Country for the branch.                                                                                                                                                    | varchar(35)  |
| “ShipToCounty”                | Ship-to County for the branch.                                                                                                                                                     | varchar(35)  |
| "Remit-to Address 1"          | Remit-to Address - Line 1 for the branch.                                                                                                                                          | varchar(100) |
| "Remit-to Address 2"          | Remit-to Address - Line 2 for the branch.                                                                                                                                          | varchar(100) |
| "Remit-to City"               | Remit-to City for the branch.                                                                                                                                                      | varchar(100) |
| "Remit-to Region"             | Remit-to Region for the branch.                                                                                                                                                    | varchar(6)   |
| "Remit-to Postal Code"        | Remit-to Postal Code for branch.                                                                                                                                                   | varchar(6)   |
| "Remit-to Country"            | Remit-to Country for the branch.                                                                                                                                                   | varchar(35)  |
| "Remit-to County”             | Remit-to County for the branch.                                                                                                                                                    | varchar(35)  |
| “Contact Salutation”          | Salutation used for the branch contact (ie, Mr., Mrs., Ms, etc).                                                                                                                   | varchar(50)  |
| “ContactFirstName”            | First Name of the branch contact.                                                                                                                                                  | varchar(100) |
| “ContactMiddleInitial”        | Middle Initial of the branch contact.                                                                                                                                              | varchar(1)   |
| “ContactLastName”             | Last Name of the branch contact.                                                                                                                                                   | varchar(100) |
| “ContactTitle”                | Title of the branch contact (ie, President, Sales Manager, Director, etc)                                                                                                          | varchar(50)  |
| “ContactWorkPhone”            | Work phone number of the branch contact, including dashes and spaces.                                                                                                              | varchar(30)  |
| “ContactFax”                  | Fax number of the branch contact, including dashes and spaces.                                                                                                                     | varchar(30)  |
| "Contact Home Phone"          | Home phone number of the branch contact, including dashes and spaces.                                                                                                              | varchar(30)  |
| "Contact Pager"               | Pager number of the branch contact, including dashes and spaces.                                                                                                                   | varchar(30)  |
| "Contact E-mail Address"      | Email address for the branch contact; multiple email addresses are separated with a semicolon ( ; ).                                                                               | varchar(100) |
| "Contact Ship-to Address 1"   | Ship-to Address - Line 1 for the branch contact.                                                                                                                                   | varchar(100) |
| "Contact Ship-to Address 2"   | Ship-to Address - Line 2 for the branch contact.                                                                                                                                   | varchar(100) |
| "Contact Ship-to City"        | Ship-to City for the branch contact.                                                                                                                                               | varchar(100) |
| "Contact Ship-to Region"      | Ship-to Region for the branch contact.                                                                                                                                             | varchar(6)   |
| "Contact Ship-to Postal Code" | Ship-to Postal Code for the branch contact.                                                                                                                                        | varchar(6)   |
| "Contact Ship-to Country"     | Ship-to Country for the branch contact.                                                                                                                                            | varchar(35)  |
| "Contact Ship-to County"      | Ship-to County for the branch contact.                                                                                                                                             | varchar(35)  |
| "Legacy Company"              | Legacy Company associated with the branch.                                                                                                                                         | varchar(10)  |
| "Legacy Branch"               | Legacy Branch associated with the branch.                                                                                                                                          | varchar(48)  |
| "Legacy Customer Base Branch" | Legacy Customer Base Branch associated with the branch.                                                                                                                            | varchar(10)  |
| "G/L Branch"                  | G/L Branch associated with the branch.                                                                                                                                             | varchar(10)  |
| "A/P Branch"                  | A/P Branch associated with the branch.                                                                                                                                             | varchar(10)  |
| "Non-Sales Branch"            | When set to TRUE, this field indicates that this branch does not sell trucks using Karmak software, but does use the Parts and/or Service modules.                                 | bit          |
| "Is Book Branch"              | When set to TRUE, this field indicates that this branch owns its own equipment and posts the inventory value.                                                                      | bit          |
| "Book Branch”                 | Book Branch associated with this branch; this field is disabled in the application when “Is Book Branch” = TRUE.                                                                   | varchar(10)  |
| "SM Next Invoice Number"      | Next invoice number assigned to a deal packet invoice created in the branch (Sales).                                                                                               | int          |
| "SM Invoice Prefix"           | Alpha-numeric prefix to assign to the front of invoice numbers for every deal packet invoice created in the branch (Sales).                                                        | varchar(4)   |
| "SM Invoice Suffix"           | Alpha-numeric suffix to assign to the end of invoice numbers for every deal packet invoice created in the branch (Sales).                                                          | varchar(4)   |
| "FET Rate”                    | Federal Excise Tax (FET) rate to charge for the branch; up to 8 digits (\#\#.\#\#\#\#\#\#).                                                                                        | decimal      |
| "Unit Cost Conversion"        | Indicates when the branch converts cost of the unit from the foreign currency to the local currency; Accounting Posted, Invoice, Receive Invoice, or Unit Added to Quote           | varchar(50)  |
| "LPO Cost Conversion"         | Indicates when the branch converts cost of the LPO from the foreign currency to the local currency; Accounting Posted, Invoice, or Unit Added to Quote                             | varchar(50)  |
| "A/P Vendor Control Branch"   | A/P Vendor Control Branch associated with the branch.                                                                                                                              | varchar(10)  |
| "Add User"                    | Username associated with the user who added the branch record.                                                                                                                     | varchar(20)  |
| "Add Date"                    | Date/time the branch record was added.                                                                                                                                             | datetime     |
| "Last Update User"            | Username associated with the user who most recently updated the branch record.                                                                                                     | varchar(20)  |
| "Last Update Date"            | Date/time the branch record was most recently updated.                                                                                                                             | datetime     |

 
#### METHOD GET
```json
/frw/Branch
```

#### Sample Branch API Response

```json
{
	"Branch Code": "01",
	"Name": "New Truck",
	"Inactive": false,
	"Division": "Future1",
	"Division Admin Branch": false,
	"Corporate Admin Branch": false,
	"Federal Tax ID": "371112601",
	"Region Tax ID": "",
	"Office Phone": "",
	"Shop Phone": "123-456-7890",
	"Parts Phone": "800-655-3281",
	"Fax": "800-123-4444",
	"E-mail Address": " <info@karmak.com>",
	"Web Address": "",
	"Bill-to Address 1": "BT 1301 East 64th Avenue XXXXX",
	"Bill-to Address 2 ": "2",
	"Bill-to City": "Hagerstown",
	"Bill-to Region": "TX",
	"Bill-to Postal Code": "99518",
	"Bill-to Country": "",
	"Bill-to County": "",
	"Ship-to Address 1": "1 Corvette Dr",
	"Ship-to Address 2": "Floor \#23",
	"Ship-to City": "Orlando",
	"Ship-to Region": "TX",
	"Ship-to Postal Code": "63101",
	"Ship-to Country": "",
	"Ship-to County": "Greene",
	"Remit-to Address 1": "1301 East 64th Avenue",
	"Remit-to Address 2": "Address line 2",
	"Remit-to City": "St Louis",
	"Remit-to Region": "AL",
	"Remit-to Postal Code": "63101",
	"Remit-to Country": "canada",
	"Remit-to County": "Macoupin",
	"Contact Salutation": "",
	"Contact First Name": "Richard",
	"Contact Middle Initial": " ",
	"Contact Last Name": "Schien......",
	"Contact Title": "",
	"Contact Work Phone": "800-111-1111",
	"Contact Fax": "800-222-2222",
	"Contact Home Phone": "800-333-3333",
	"Contact Pager": "800-444-4444",
	"Contact E-mail Address": "<csellers@karmak.com>",
	"Contact Web Address": "[WWW.NewTruckSales2.com](http://WWW.NewTruckSales2.com)",
	"Contact Ship-to Address 1": "",
	"Contact Ship-to Address 2": "",
	"Contact Ship-to City": "",
	"Contact Ship-to Region": "",
	"Contact Ship-to Postal Code": "",
	"Contact Ship-to Country": "",
	"Contact Ship-to County": "",
	"Legacy Company": "020",
	"Legacy Branch": "",
	"Legacy Customer Base Branch": "",
	"G/L Branch": null,
	"A/P Branch": null,
	"Non-Sales Branch": "01",
	"Is Book Branch": true,
	"Book Branch": "01",
	"SM Next Invoice Number": 2923,
	"SM Invoice Prefix": "",
	"SM Invoice Suffix": "",
	"FET Rate": 12.0000,
	"Unit Cost Conversion": "Receive Invoice",
	"LPO Cost Conversion": "Unit Added to Quote",
	"A/P Vendor Control Branch": "01",
	"Add User": null,
	"Add Date": "2004-02-02T00:00:00",
	"Last Update User": "demo",
	"Last Update Date": "2019-07-02T16:37:39.270"
}
```
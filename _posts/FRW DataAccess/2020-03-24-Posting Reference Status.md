---
layout: post
title: "Posting Reference Status"
category: "Accounts Payable" 
icon: "icon-shopping-bag"
type: "data_access"
comments: false
description:   Allow the user to query the status of a posting reference, including whether or not the P/O has been received, if it has been referenced on an A/P invoice, and if the A/P Invoice has been posted.
---

---

---

A GET API to query the status of a posting reference, including whether or not the P/O has been received, if it has been referenced on an A/P invoice, and if the A/P Invoice has been posted.

| Field | Definition | Type |
|---|---|---|
| “BranchCode”   | Branch associated with the purchase order or invoice.                                                                                                                                                           | varchar(10) |
| “Department”   | Department associated with the purchase order or invoice.                                                                                                                                                       | varchar(10) |
| “PONumber”     | Purchase Order Number associated with the reference; includes Parts Purchase Order, Miscellaneous Purchase Order, and Local Purchase Order.                                                                     | varchar(30) |
| “SupplierCode” | Supplier associated with the purchase order or invoice.                                                                                                                                                         | varchar(20) |
| “APVendor”     | A/P Vendor associated with the purchase order or invoice.                                                                                                                                                       | varchar(10) |
| “APVendorID”   | Unique database ID of the A/P Vendor associated with the purchase order or invoice.                                                                                                                             | int         |
| “EntityID”     | Unique database ID of the reference; can be Parts Receiving Reference number, Miscellaneous Purchase Order number, or Local Purchase Order number.                                                              | int         |
| “Reference”    | Reference number associated with the purchase order or invoice; includes Parts Receiving Reference number, Miscellaneous Purchase Order number, and Local Purchase Order number.                                | varchar(50) |
| “PackingSlip”  | Packing Slip number associated with the purchase order received.                                                                                                                                                | varchar(50) |
| “PODate”       | Date the Purchase Order was finalized.                                                                                                                                                                          | datetime    |
| “POStatus”     | Status of the Purchase Order; ‘Open’ statuses include: *Suggested P/O, In Process, Return in Process*; ‘Finalized' statuses include: *Finalized Return, On Order, Partial, Received*.                           | varchar(50) |
| “IsReferenced” | When set to TRUE, the posting reference has been referenced on an A/P Invoice.                                                                                                                                  | bit         |
| “EntityTypeID” | Database ID that denotes the type of reference; LPO (12), MPO (46), or Parts Receiving (104).                                                                                                                   | int         |
| “EntityType”   | Description of the type of reference; LPO, MPO, or Parts Receiving.                                                                                                                                             | varchar(50) |
| “ReceivedDate” | Received date from the detail line of a Parts Receiving Reference - if parts are received on multiple dates, this will always pull the last received (most recent) date; for MPOs and LPOs, this field is NULL. | datetime    |
| “Amount”       | Total reference amount; for Parts Receiving references - the sum of Extended Cost and Core Extended Cost (Total); for MPOs - the Total from the MPO header; for LPOs, the Expected Amount.                      | decimal     |
| “APStatus”     | Status of the A/P Invoice; *Not Posted, Posted, Paid.*                                                                                                                                                          | varchar(10) |

#### Sample Response
```json
{
	"BranchCode": "01",
	"Department": "",
	"PONumber": "3079",
	"SupplierCode": "Q'STRAINTN",
	"APVendor": "01222",
	"APVendorID": 4,
	"EntityID": 41,
	"Reference": "10039",
	"PackingSlip": "8018751721",
	"PODate": "2013-04-10T08:04:04.597",
	"POStatus": "Received",
	"IsReferenced": false,
	"EntityTypeID": 104,
	"EntityType": "Parts Receiving",
	"ReceivedDate": "2013-04-10T08:39:49.943",
	"Amount": 8.25,
	"APStatus": "Not Posted"
}
```
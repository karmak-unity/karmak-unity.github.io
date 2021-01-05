---
layout: post
title: "A/P Invoice"
category: "Accounting" 
icon: "icon-credit-card1"
type: "api" 
comments: false
description:  Accounts Payable invoices that do not flow through the existing Fusion '810' invoice path
---

---
This supports Accounts Payable invoices that do not flow through the existing Fusion '810' invoice path.  This includes all invoice types (Parts P/O, Non-P/O, MPO, and LPO), as of a 3.59.0.0 enhancement. Multiple invoices can be sent in a single POST request 

__Note: minimum fusion version 3.59.0.0 (updated 12.19.2019)__


### POST Request
```
https://api.karmak.io/api/unity/{version}/unityapi/ap/invoice
```

Note: API Version; v1 as of June 30, 2019



### Specifications

* User must identify an Action of Save or Post
	* Save indicates that the A/P invoice will be created in Fusion, but will not yet be posted to the General Ledger.  Saved invoices will need to be manually posted by the user in Fusion.
	* Post indicates that the A/P Invoice will be created in Fusion, and will be posted to the General Ledger.
	
* User must identify an Invoice Type
	*	PARTSPO = invoices associated with a purchase order number
		* If Invoice Type = PARTSPO, a reference number must be supplied 
	*	NONPO = invoices with no associated purchase order number.
	*	MPO = invoices associated with a Miscellaneous Purchase Order
	*	LPO = invoices associated with a Local Purchase Order
		*	Note that Multiple LPOs cannot be associated with a single invoice

### Invoice Creation Rules & Exceptions

*    If invoice amount does not equal the sum of the total details, invoice will be rejected and error returned to sender.
*    If detail lines to do not sum to zero (invoice is out of balance)
        * When Action = Save, invoice will be created out of balance; return message to sender that invoice was created out of balance. (Fusion allows invoices to be created and saved out of balance.)
        * When Action = Post,and G/L lines do not balance, the action is changed to 'Save' and status returned = Not Posted.
*    When the invoice is created, Fusion looks for the existence of the payables line in the inbound invoice
        * If the payables line is present, the invoice must be in balance
        * If the payables line is not present, and the invoice is in balance, the invoice will be rejected.
        * If the payables line is not present, and the invoice is not in balance, the payables line will be added as part of Fusion logic.
*    If Invoice Type = MPO, and no MPO number is provided
        * Invoice will be rejected and error returned to sender that MPO number is required when Invoice Type = MPO.
*    If Invoice Type = NONPO, and a P/O Number is supplier
        * Invoice will be rejected and error returned that Invoice Type = NONPO cannot be associated with a Purchase Order Number.
*    If Invoice Type = LPO and no LPO number is provided
        * Invoice will be rejected and error returned to sender that LPO number is required when Invoice Type = LPO.

### Invoice Validation Rules & Exceptions
#### Controlled Account Validation

When Controlled G/L Accounts are used, the account must be validated against the appropriate control value.

*    Control Types
     *   No Validation
      *  Entity Validation - validated against a Fusion data table
      *  Validation List - validated against a customer-defined QuickList of data created in Fusion 
*    If the G/L Account is controlled, the correct control value must be passed in the Control field in the API.
*    Available Validation Entities
     *   Customer 
     *   Fixed Asset 
     *   Parts Order Invoice Number
     *   Repair Order Invoice Number
     *   Repair Order Number
     *   Stock Number
     *   Unit Number
     *   Unit Purchase Order Number

|JSON API MAP|Description|Length / Format|Required?|Default (if not sent)|    
|--------------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
|InvoiceDate                    | Vendor invoice date                                                                                        | mmddyyyy                                      |                                      | Today's date                                                                                                                                      |
|InvoiceNumber                  | Vendor invoice number                                                                                      | Up to 250 alpha-numeric characters            | Required                             |                                                                                                                                                           |
|InvoiceType                    | Type of invoice being passed; MPO, LPO, NONPO, PARTSPO                                                     |                                               | Required                             |                                                                                                                                                           |
|AccountingPeriodID				| Accounting Period to post the invoice to																	 | numeric  |
|Action                         | Action associated with the invoice; SAVE to create/save the invoice, POST to create/save/post the invoice. |                                               | Required                             |                                                                                                                                                           |
|ApVendor                       | Vendor associated with the invoice                                                                         | Up to 20 alpha-numeric characters             | Required                             |                                                                                                                                                           |
|InvoiceAmount                  | Invoice amount                                                                                             | Up to 9 digits, with decimal                  | Required                             |                                                                                                                                                           |
|PaymentTerms                   | Vendor Payment Terms                                                                                       | Up to 50 alpha-numeric or special characters  |                                      | A/P Vendor default Payment Terms                                                                                                                          |
|DueDate                        | Invoice Due date                                                                                           | mmddyyyy                                      |                                      | Current system date or calculates from invoice date/payment terms if:  <BR> -   due date is omitted<BR> -   due date = null<BR> -   due date = 1/1/1900                                                                                          |
|DiscountAmount                 | Invoice discount amount                                                                                    | Up to 20 digits, including decimal            |                                      | Calculated using discount percentage for payment term and invoice amount                                                                                  |
|PostingDescription             | Invoice posting description                                                                                | Up to 250 alpha-numeric or special characters |                                      | Vendor number + Invoice number                                                                                                                            |
|PostingBranch                  | Reference Branch associated with the invoice                                                               |                                               | Required                             | User's branch                                                                                                                                             |
|ReferenceNumber                | Reference number associated with the invoice                                                               |                                               | Required when Invoice Type = PARTSPO |                                                                                                                                                           |
|GlBranch                   | G/L Branch for the transaction                                                                             | Up to 10 alpha-numeric characters             |                                      | Required when Action = Post <BR> Not Required when Action = Save                                                                                               |
|GlAccount                  | G/L account to which the transaction will post                                                             |                                               |                                      | Required when Action = Post <BR> Not Required when Action = Save                                                                                               |
|Department                 | G/L department                                                                                             |                                               |                                      | Required when Action = Post *and* G/L used is departmentalized Not Required when Action = Save, <BR>Will ignore if sent with a G/L that is not departmentalized                                                            |
|DebitAmount                | Debit amount for the invoice; no decimal places are assumed if decimal is not entered                      | Up to 10 numeric characters                   |                                      | Required when Action = Post <BR> Not Required when Action = Save                                                                                               |
|CreditAmount               | Credit amount for the invoice; no decimal places are assumed if decimal is not entered                     | Up to 10 numeric characters                   |                                      | Required when Action = Post <BR> Not Required when Action = Save                                                                                               |
|OverridePostingDescription | Posting description for the detail transaction line                                                        |                                               |                                      |                                                                                                                                                           |
|Control                    | Control value for G/L Account, if G/L Account is controlled                                                |                                               |                                      |                                                                                                                                                           |
|Allocation                 | Allocation table to be associated with the G/L's account detail line item                                  | Up to 250 alpha-numeric characters            |                                      | If allocation is not passed, and the account has a default allocation, the default allocation will be used                                                |


### Sample Request
```json	
[
  {
    "InvoiceDate": "2019-04-01",
    "InvoiceNumber": "I1234",
    "InvoiceType" : "MPO",
    "Action" : "Post",
    "ApVendor": "01222",
    "InvoiceAmount": 25.00,
    "PaymentTerms": "30 days, 2% 10 days",
    "DueDate": "2019-05-02",
    "DiscountDate" : "2019-04-10",
    "DiscountAmount": 0.05,
    "PostingDescription": "Vendor 01222 Invoice I1234",
    "PostingBranch": "01",
    "ReferenceNumber": "123",
    "Details": [
      {
        "GlBranch": "01",
        "GlAccount": "2040",
        "Department": "",
        "DebitAmount": 0.00,
        "CreditAmount": 25.00,
        "OverridePostingDescription": "Accounts Payable - Vehicle Accrual",
        "Control": "",
        "Allocation": ""
      },
      {
        "GlBranch": "01",
        "GlAccount": "1400",
        "Department": "",
        "DebitAmount": 25.00,
        "CreditAmount": 0.00,
        "OverridePostingDescription": "Inventory-Parts",
        "Control": "",
        "Allocation": ""
      }
    ]
  },
  {
    "InvoiceDate": "2019-04-01",
    "InvoiceNumber": "I1234-lpo",
    "InvoiceType" : "LPO",
    "Action" : "Save",
    "ApVendor": "10490",
    "InvoiceAmount": 4300.00,
    "PaymentTerms": "Net 30th",
    "DueDate": "2019-05-30",
    "PostingDescription": "Vendor 10490 Invoice I1234-lpo",
    "ReferenceNumber": "5415",
    "Details": [
      {
        "GlBranch": "01",
        "GlAccount": "2000",
        "Department": "",
        "DebitAmount": 0.00,
        "CreditAmount": "4300.00",
        "OverridePostingDescription": "Accounts Payable - Vehicle Accrual",
        "Control": "",
        "Allocation": ""
      },
      {
        "GlBranch": "01",
        "GlAccount": "8015",
        "Department": "New Trlr",
        "DebitAmount": 4300.00,
        "CreditAmount": 0.00,
        "OverridePostingDescription": "Inventory-Parts",
        "Control": "",
        "Allocation": ""
      }
    ]
  }
]
```

#### Possible response codes

|Code|Description|
|---|---|
|201	Created|	The a/p invoice was created successfully in Fusion|
|400	Bad Request|	There was a validation or business rule violation that prevented the invoice from being created|
|500	internal service error|	This would indicate an unexpected and unrecoverable problem was encountered. Details should be logged.|
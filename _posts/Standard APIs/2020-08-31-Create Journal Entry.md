---
layout: post
title: "Create Journal Entry"
category: "Accounting"
icon: "icon-credit-card1"
type: "api"
comments: false
description: Create a Journal Entry that will post
---

The Create Journal Entry API is used to create a journal entry and post it to accounting transaction if there are no errors.


***NOTE: Requires Fusion version 3.60.30***

### Specifications

#### POST

When processing the journal entry passed to the API it is processed as a journal
entry that will post and create a posted accounting trasnaction on the business
system and, if successful, the posting sequence is returned.

##### Validations for G/L Transaction

-   If here are any errors in the entry we will look at the value sent for
    SaveOnError. If this value doesn’t equal Y we will not save the journal
    Entry. We will return an error that there were errors and that it was/wasn’t
    saved based on the parameter.

-   If the posting period we are passed is closed we will not post the
    transaction

-   If the posting period is a future posting period we will not post the
    transaction

### Request Fields

| **Name**                   | **Max Length** | **Required** | **Description**                                                                                                                                              | **Verifications**                                                                                                                                                                                 |
|----------------------------|----------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SaveOnError                | True/False     | N            | Defines if we save a journal entry that has any errors                                                                                                       |   |
| Journal                    | 50             | Y            | Journal – defaults to General Journal if nothing entered. There are other string values that an be sent                                                      |   |
| JournalReference           | 250            | Y            | Description for Journal Reference.                                                                                                                           |   |
| postingDescription         | 250            | Y            | Description of posting being performed. Defaults to Journal Reference sent in if left blank                                                                  |   |
| PostingBranch              | 10             | Y            | The branch the posting is for                                                                                                                                | Verify branch is not Inactive                                                                                                                                                                     |
| TransactionDate            | 8              | Y            | Date transaction took place. Value should be MMDDYYYY                                                                                                        |   |
| PostingPeriodID            |    | Y            | Accounting period we are posting the transaction to.                                                                                                         | Use transaction date to verify if the posting period is closed or in the future                                                                                                                   |
| CommentType                | 10             | Dependent    | The comment type associated with the comment being sent                                                                                                      |   |
| BriefDescription           | 50             | Dependent    | The brief description for the comment being created.                                                                                                         | If a comment is sent in and there is no brief description we will populate the field with the first 50 characters of the Comment                                                                  |
| Comment                    | 7500           | Dependent    | The comment being sent it                                                                                                                                    |   |
| Branch                     | 10             | Y            | The branch the detail line item is for                                                                                                                       | Verify the branch is not Inactive                                                                                                                                                                 |
| GeneralLedgerAccount       | 20             | Y            | The g/l account the line item detail is for                                                                                                                  | Verify the g/l account is not Inactive Verify if account is departmentalized. If it is departmentalized we will need a department below.                                                          |
| Department                 | 10             | Dependent    | The department the line item detail is for, if the account is departmentalized                                                                               | Verify department is not Inactive and is assigned to the Branch value above                                                                                                                       |
| DebitAmount                | 20             | Dependent    | If debit amount - credit amount \>= 0.00 we will post a debit otherwise it will be a credit Field allows 17 to the left of the decimal and 2 decimal places. |   |
| CreditAmount               | 20             | Dependent    | If debit amount - credit amount \>= 0.00 we will post a debit otherwise it will be a credit Field allows 17 to the left of the decimal and 2 decimal places. |   |
| OverRidePostingDescription | 250            | N            | Line item specific posting description                                                                                                                       |   |
| Control                    | 50             | Dependent    | Control value for the line item                                                                                                                              |   |
| Allocation                 | 250            | N            | Allocation for the line item                                                                                                                                 | If allocation has departments associated with it we need to verify g/l account is set to departmentalized = true If g/l account has a default allocation we will override with the value sent in. |


### REQUEST POST URL
```
.../unityapi/GeneralLedger/JournalEntry
```


### POST Request
```json
[{
	"journal": {
		"ID": "",
		"reference": "description for journal"
	},
	"description": "",
	"branchID": "",
	"date": "MMDDCCYY",
	"postingPeriodID": "",
	"saveOnError": "",
	"lineItems": [{
			"branchID": "",
			"glAccountID": "",
			"departmentID": "",
			"allocationID": "",
			"amount": "",
			"type": "",
			"description": "",
			"control": ""
		},
		{
			"branchID": "",
			"glAccountID": "",
			"departmentID": "",
			"allocationID": "",
			"amount": "",
			"type": "",
			"description": "",
			"control": ""
		},
		{
			"branchID": "",
			"glAccountID": "",
			"departmentID": "",
			"allocationID": "",
			"amount": "",
			"type": "",
			"description": "",
			"control": ""
		}
	]
}]
```

### POST Response
```json
{
	"journalID": "",
	"sequence": "",
	"glAccount": ""
}
```
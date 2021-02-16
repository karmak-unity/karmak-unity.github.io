---
layout: post
title: "Parts Supersession"
category: "Parts" 
icon: "icon-gear"
type: "api" 
comments: false
description:  Allow users to Create, Update and Delete Supersessions Fusion
---

---
---

The  Supersession Unity API endpoint will be created to allow users to Create, Update and Delete Supersessions Fusion.

- A Supersession record is considered a record that will allow a user to identify a valid part number in Fusion that will be replaced by another valid Part Number in Fusion.
- These records will be able to be found in the Fusion form, INV91600 Cross Reference and Supersession
 
### POST Request
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/CreateSupersession
```

### PUT Request
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/UpdateSupersession
```

### DELETE Request
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/DeleteSupersession
```


### Specifications

#### POST
-   The POST method will be used to create Supersession records in Fusion.
-   Only one Supersession record will be allowed in a single request call.
-   A combination of the following must be passed in to identify a unique record when attempting to create a Supersession record.  If one of these combinations aren’t passed in the Request should fail.
	- From Part Number, From Supplier, Branch, To Part Number, To Supplier
	- From Part Number, From Supplier, All Branches, To Part Number, To Supplier
-   A response will be provided with a message section that will outline a success or any issues that prevented the Supersession from being created.
-   The Fusion Username used in the Unity API call will be used as the Add and Last Update User of the Supersession created.
-   The Date and Time the Unity API call was made will be used as the Add Date and Last Update of the Supersession created.
-   The Supersession record will be created in Fusion following the standard create logic of the INV91600 Cross Reference and Supersession form in Fusion outside of any specific rules listed in this section and the POST/PUT Request Fields Section below.

#### PUT
-   The PUT method will be used to update Supersession records in Fusion.
-   Only one Supersession record will be allowed in a single request call.
-   A combination of the following must be passed in the Supersession Identity section to identify a unique record when attempting to update a Supersession record.  If one of these combinations aren’t passed in the Request should fail.
	- From Part Number, From Supplier, Branch, To Part Number, To Supplier
	- From Part Number, From Supplier, All Branches, To Part Number, To Supplier
-   A response will be provided with a message section that will outline a success or any issues that prevented the supersession from being updated.
-   The Fusion Username used in the Unity API call will be used as the Last Update User of the Supersession updated.
-   The Date and Time the Unity API call was made will be used as the Last Update Date of the Supersession updated.

#### DELETE
-   The DELETE method will be used to delete Supersession records in Fusion.
-   Only one Supersession record will be allowed in a single request call.
-   A combination of the following must be passed in the Supersession Identity section to identify a unique record when attempting to delete a Supersession record.  If one of these combinations aren’t passed in the Request should fail.
    - From Part Number, From Supplier, Branch, To Part Number, To Supplier
	- From Part Number, From Supplier, All Branches, To Part Number, To Supplier
-   A response will be provided with a message section that will outline a success or any issues that prevented the Supersession from being deleted.

### POST/PUT/DELETE Request Fields

| Field       | Field Type | Required | Length | POST Business Rules and Defaults    | PUT Business Rules and Defaults       | Delete Business Rules and Defaults    |
|-------------|------------|----------|--------|-------------------------------------|---------------------------------------|---------------------------------------|
| **Supersession Identity**                                                     | Node           |  |      | This section will be ignored in a POST when creating a Supersession record.                                                                                                                                                                                                                                                                                                                           | This section will be used to identity the Supersession record being looked up to update                                                                                                                                                                                                                                                                                                               | This section will be used to identify Supersession record being looked up to delete All values in the Main Body section will be ignored.  |
| From Part Number                                                              | String         | Yes          | 50         | | This is the From Part Number being looked up to find the Supersession record to be updated.                                                                                                                                                                                                                                                                                                           | This is the From Part Number being looked up to find the Supersession record to be deleted.                                               |
| From Supplier                                                                 | String         | Yes          | 20         | | This is the Supplier the From Part Number will be looked up in.                                                                                                                                                                                                                                                                                                                                       | This is the Supplier the From Part Number will be looked up in.                                                                           |
| Branch                                                                        | String         | Yes          | 10         | | This is the Branch being looked up to find the Supersession record to be updated.                                                                                                                                                                                                                                                                                                                     | This is the Branch being looked up to find the Supersession record to be deleted.                                                         |
| All Branches                                                                  | Boolean        | Yes          | 1          | | This is All Branches checkbox value that will be looked up to find the Supersession record to be updated.                                                                                                                                                                                                                                                                                             | This is All Branches checkbox value that will be looked up to find the Supersession record to be deleted.                                 |
| To Part Number                                                                | String         | Yes          | 50         | | This is the To Part Number being looked up to find the Supersession record to be updated.                                                                                                                                                                                                                                                                                                             | This is the To Part Number being looked up to find the Supersession record to be deleted.                                                 |
| To Supplier                                                                   | String         | Yes          | 20         | | This is the Supplier the To Part Number will be looked up in.                                                                                                                                                                                                                                                                                                                                         | This is the Supplier the To Part Number will be looked up in.                                                                             |
| **Main Body**                                                                 |    |  |      | | | |
| From Part Number                                                              | String         | Yes          | 50         | This is the From Part Number the Supersession record is being created for.  This must be a valid active Part Number setup in Fusion.                                                                                                                                                                                                                                                                  | This is the From Part Number the Supersession record is being updated for.  This must be a valid active Part Number setup in Fusion.                                                                                                                                                                                                                                                                  | |
| From Supplier                                                                 | String         | Yes          | 20         | This is the Supplier the From Part Number is being looked up.                                                                                                                                                                                                                                                                                                                                         | This is the Supplier the From Part Number is being looked up.                                                                                                                                                                                                                                                                                                                                         | |
| From Branch                                                                   | String         | Dependent    | 10         | This is the Branch the From Part Number is being looked up in.  If the All Branches checkbox is set to True then this field will be ignored.  If this field is not sent or left blank then the user would need to set the All Branches field to 1.                                                                                                                                                    | This is the Branch the From Part Number is being looked up in.  If the All Branches checkbox is set to True then this field will be ignored.  If this field is not sent or left blank then the user would need to set the All Branches field to 1.                                                                                                                                                    | |
| All Branches                                                                  | Boolean        | Dependent    | 1          | This field will determine if the Supersession record being created is for all Branches or not.  This field will allow a 1 to indicate it will be for all Branches or 0 to indicate it is for a single branch identified in the Branch Field.  If this field is set to 1 then the Branch field will be ignored.  If this field is set to 0, blank or missing then the Branch field will be required.   | This field will determine if the Supersession record being updated is for all Branches or not.  This field will allow a 1 to indicate it will be for all Branches or 0 to indicate it is for a single branch identified in the Branch Field.  If this field is set to 1 then the Branch field will be ignored.  If this field is set to 0, blank or missing then the Branch field will be required.   | |
| To Part Number                                                                | String         | Yes          | 50         | This is the To Part Number the Supersession is being created for.  This must be a valid active Part Number setup in Fusion.                                                                                                                                                                                                                                                                           | This is the To Part Number the Supersession is being updated for.  This must be a valid active Part Number setup in Fusion.                                                                                                                                                                                                                                                                           | |
| To Supplier                                                                   | String         | Yes          | 20         | This is the Supplier the To Part Number will be looked up in.                                                                                                                                                                                                                                                                                                                                         | This is the Supplier the To Part Number will be looked up in.                                                                                                                                                                                                                                                                                                                                         | |
| Cross Reference Message                                                       | String         |  | 50         | This is the Cross Reference Message that will be associated with the Supersession record.  This must match a valid Cross Reference Message setup in Fusion.                                                                                                                                                                                                                                           | This is the Cross Reference Message that will be associated with the Supersession record.  This must match a valid Cross Reference Message setup in Fusion.                                                                                                                                                                                                                                           | |
| Print Message on Invoice                                                      | Boolean        |  | 1          | This field will indicate whether to set the Print Message on Invoice checkbox to on or off.  Send a 1 to turn this on.  Don’t send this field, leave blank or send zero to indicate this will be turned off. This will be ignored if the Cross Reference Message field is left blank or not passed in.  The Default will be to leave this turned off.                                                 | This field will indicate whether to set the Print Message on Invoice checkbox to on or off.  Send a 1 to turn this on.  This will be ignored if the Cross Reference Message field is left blank or not passed in.                                                                                                                                                                                     | |
| Supersession Type                                                             | String         |  | 10         | This field will indicate what type of Supersession is being created.  Valid options are; Immediate, Date, Zero Available.  If the value isn’t passed in or isn’t one of the valid values it will default to “Zero Available”.                                                                                                                                                                         | This field will indicate what type of Supersession is being created.  Valid options are; Immediate, Date, Zero Available.                                                                                                                                                                                                                                                                             | |
| Move Picks and Sales when superseded                                          | Boolean        |  | 1          | This field determines whether to move picks and sales of the From Part Number when the supersession happens.  Send a 1 to indicate Yes or 0 to indicate No. If the value isn’t passed in the default will be set to 1.                                                                                                                                                                                | This field determines whether to move picks and sales of the From Part Number when the supersession happens.  Send a 1 to indicate Yes or 0 to indicate No.                                                                                                                                                                                                                                           | |
| Move Picks and Sales immediately                                              | Boolean        |  | 1          | This field determines whether to move picks and sales of the From Part Number immediately.  Send a 1 to indicate Yes or 0 to indicate No. If the value isn’t passed in the default will be set to 1. This value will be ignored if the Supersession Type is Immediate.                                                                                                                                | This field determines whether to move picks and sales of the From Part Number immediately.  Send a 1 to indicate Yes or 0 to indicate No.  This value will be ignored if the Supersession Type is Immediate.                                                                                                                                                                                          | |
| Change from part stock status when superseded                                 | Boolean        |  | 1          | This field determines whether to change the From Part Stock Status when the supersession happens.  Send a 1 to indicate Yes or 0 to indicate No. If the value isn’t passed in the default will be set to 1.                                                                                                                                                                                           | This field determines whether to change the From Part Stock Status when the supersession happens.  Send a 1 to indicate Yes or 0 to indicate No.                                                                                                                                                                                                                                                      | |
| Change from part stock status immediately                                     | Boolean        |  | 1          | This field determines whether to change the From Part Stock Status immediately.  Send a 1 to indicate Yes or 0 to indicate No. If the value isn’t passed in and Supersession Type is Date or Quantity the default will be set to 0. This value will be ignored if the Supersession Type is Immediate.                                                                                                 | This field determines whether to change the From Part Stock Status immediately.  Send a 1 to indicate Yes or 0 to indicate No. This value will be ignored if the Supersession Type is Immediate.                                                                                                                                                                                                      | |
| Change Open Purchase Order and Customer Backorder information when superseded | Boolean        |  | 1          | This field determines whether to change the Open Purchase Order and Customer Backorder information for the From Part when the supersession happens.  This field will always be ignored and set to 1.                                                                                                                                                                                                  | This field determines whether to change the Open Purchase Order and Customer Backorder information for the From Part when the supersession happens.  This field will always be ignored and set to 1.                                                                                                                                                                                                  | |
| Change Open Purchase Order and Customer Backorder information immediately     | Boolean        |  | 1          | This field determines whether to change the Open Purchase Order and Customer Backorder information for the From Part immediately.  Send a 1 to indicate Yes or 0 to indicate No. If the value isn’t passed in and Supersession Type is Date or Quantity the default will be set to 0. This value will be ignored if the Supersession Type is Immediate.                                               | This field determines whether to change the Open Purchase Order and Customer Backorder information for the From Part immediately.  Send a 1 to indicate Yes or 0 to indicate No. This value will be ignored if the Supersession Type is Immediate.                                                                                                                                                    | |
| Supersession Date                                                             | Date           |  |      | This is the date the Supersession will occur on. This will be ignored if the Supersession Type isn’t Date. If the Supersession Type is Date and the value isn’t passed in or is left blank then default to the Current Date the Supersession record is being created for.                                                                                                                             | This is the date the Supersession will occur on. This will be ignored if the Supersession Type isn’t Date. If the Supersession Type is Date and the value isn’t passed in or is left blank then default to the Current Date the Supersession record is being created for.                                                                                                                             | |
| Move Part Available quantities when superseded                                | Boolean        |  | 1          | This field determines whether to move the quantity available of the From Part when the supersession happens.  Send a 1 to indicate Yes or 0 to indicate No. If the value isn’t passed in the default will be set to 1. This value be set to 1 and ignored if the Supersession Type is Immediate.                                                                                                      | This field determines whether to move the quantity available of the From Part when the supersession happens.  Send a 1 to indicate Yes or 0 to indicate No. This value be set to 1 and ignored if the Supersession Type is Immediate.                                                                                                                                                                 | |
| Move Part Available quantities immediately                                    | Boolean        |  | 1          | This field determines whether to move the quantity available of the change From Part immediately.  Send a 1 to indicate Yes or 0 to indicate No. If the value isn’t passed in and Supersession Type is Date or Quantity the default will be set to 0. This value will be ignored if the Supersession Type is Immediate.                                                                               | This field determines whether to move the quantity available of the change From Part immediately.  Send a 1 to indicate Yes or 0 to indicate No. This value will be ignored if the Supersession Type is Immediate.                                                                                                                                                                                    | |
| New Stock Status                                                              | String         |  | 10         | This will be the new Stock Status of the From Part when the Supersession takes place. If this value isn’t passed in it will default to “Superseded” Valid options are Blank, Superseded, Stock, Obsolete, Non-Stock                                                                                                                                                                                   | This will be the new Stock Status of the From Part when the Supersession takes place. Valid options are Blank, Superseded, Stock, Obsolete, Non-Stock                                                                                                                                                                                                                                                 | |
| Set from part number to inactive                                              | Boolean        |  | 1          | This field will determine if the From Part Number will be set to Inactive when the Supersession happens. If this isn’t passed in or is left blank then default to 1 for Yes.                                                                                                                                                                                                                          | This field will determine if the From Part Number will be set to Inactive when the Supersession happens.                                                                                                                                                                                                                                                                                              | |

### POST JSON Request Sample

```json
{
	"fromPartNumber":"\#10BRUSH",
	"fromSupplier":"3M",
	"fromBranch":"01",
	"toPartNumber": "3719K",
	"toSupplier":"abc",
	"supersessionType":"Zero Available",
	"supersessionDate":null,
	"movePicksandSales":true,
	"movePicksandSalesImmediate":true,
	"changeFromPartStockStatusWhenSuperseded":true,
	"changeFromPartStockStatusImmediately":false,
	"newStockStatus":"Superseded",
	"changeOpenOrderInfoWhenSuperseded":true,
	"changeOpenOrderInfoImmediately":false,
	"setFromPartInactive":true,
	"printMessageOnInvoice":false,
	"allBranches":false,
	"crossReferenceMessage":"",
	"MovePartQuantitiesWhenSuperseded":false,
	"MovePartQuantitiesImmediately":false
}
```

### POST JSON Response Sample
```json
{
	"Status": "Part supersession created successfully.",
	"Message": null
}
```

### PUT JSON Request Sample
```json
{
	"Identity":
	{
		"fromPartNumber":"WHI332644",
		"fromSupplier":"3M",
		"Branch":"03",
		"toPartNumber": "WHI332644P",
		"toSupplier":"3M"
	},
	"fromPartNumber":"MPOP2",
	"fromSupplier":"00OP2"

}
```

### PUT JSON Response Sample
```json

{
	"Status": "Part supersession updated successfully.",
	"Message": null
}
```

### DELETE JSON Request Sample
--------------------------
```json
{
	"Identity":
	{
		"fromPartNumber":"0918-1",
		"fromSupplier":"ZMA",
		"Branch":"01",
		"toPartNumber": "0918-2",
		"toSupplier":"ZMA"
	}
}
```

### DELETE JSON Response Sample
---------------------------
```json
{
	"Status": "Part supersession deleted successfully.",
	"Message": null
}
```
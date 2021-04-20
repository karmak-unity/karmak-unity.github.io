---
layout: post
title: "Parts Cross Reference"
category: "Parts" 
icon: "icon-gear"
type: "api" 
comments: false
description:  Allow users to Create, Update and Delete Cross References and Substitutions in Fusion
---

---
---

The Cross Reference Unity API endpoint will be created to allow users to Create, Update and Delete Cross References and Substitutions in Fusion.

A Cross Reference record is considered a record that allows a user to provide a text value that will cross to a valid Part Number in Fusion.

A Substitution record is considered a record that allows a user to provide a valid part number that will cross to another valid Part Number in Fusion.

These records will be able to be found in the Fusion form, INV91600 Cross Reference and Supersession

### POST Request
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/CreateCrossReference
```

### PUT Request
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/UpdateCrossReference
```

### DELETE Request
```
https://api.karmak.io/api/unity/{version}/unityapi/partsinventory/DeleteCrossReference
```

#### Specifications
--------------

**POST**
-    The POST method will be used to create Cross Reference or Substitution records in Fusion.
-    Only one Cross Reference or Substitution record will be allowed in a single request call.
-    A Combination of the following must be passed in to identity a unique record when attempting to create a Cross Reference or Substitution.  If one of these combinations aren’t passed in the Request should fail. 
     -   From Part Number, From Supplier, To Part Number, To Supplier (Substitution)
     -   Linkage Text, To Part Number, To Supplier (Cross Reference)
-    The Cross Reference Type will be defaulted to “Local” when it is created.
-    A response will be provided with a message section that will outline a success or any issues that prevented the Cross Reference or Substitution from being created.
-    The Fusion Username used in the Unity API call will be used as the Add and Last Update User of the Cross Reference or Substitution created.
-    The Date and Time the Unity API call was made will be used as the Add Date and Last Update of the Cross Reference or Substitution created.
-    The Cross Reference or Substitution record will be created in Fusion following the standard create logic of the INV91600 Cross Reference form in Fusion outside of any specific rules listed in this section and the POST/PUT Request Fields Section below.

**PUT**
-    The PUT method will be used to update Cross Reference or Substitution records in Fusion.
-    Only one Cross Reference or Substitution record will be allowed in a single request call.
-    Only fields that are expected to be updated should be passed in outside of the required fields.
-    The Cross Reference Identity section will be required to identify which record will be updated. 
-    A Combination of the following must be passed in to identity a unique record.  If one of these combinations aren’t passed in the Request should fail. 
     -   From Part Number, From Supplier, To Part Number, To Supplier (Substitution)
     -  Linkage Text, To Part Number, To Supplier (Cross Reference)
-    A response will be provided with a message section that will outline a success or any issues that prevented the Cross Reference or Substitution from being updated.
-    The Fusion Username used in the Unity API call will be used as the Last Update User of the Cross Reference or Substitution updated.
-    The Date and Time the Unity API call was made will be used as the Last Update Date of the Cross Reference or Substitution updated.
	
**DELETE**
-    The DELETE method will be used to delete Cross Reference or Substitution records in Fusion.
-    Only one Cross Reference or Substitution record will be allowed in a single request call.
-    The Cross Reference Identity section will be required to identify which record will be deleted. 
-    A Combination of the following must be passed in to identity a unique record.  If one of these combinations aren’t passed in the Request should fail. 
     -   From Part Number, From Supplier, To Part Number, To Supplier (Substitution)
     -   Linkage Text, To Part Number, To Supplier (Cross Reference)
-    A response will be provided with a message section that will outline a success or any issues that prevented the Cross Reference or Substitution from being updated.


### POST/PUT Request Fields

| Field                      | Field Type | Required | Length | POST Business Rules and Defaults                                                                                                                                                                                                                                                                                                   | **PUT Business Rules and Defaults**                                                                                                                                                                                                                                                                                                                    | **DELETE Business Rules and Defaults**                                                                                                                                                                                                                                                                        |
|--------------------------------|----------------|--------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Cross Reference Identity**   | Node           |  |      | This will be ignored in a Post when a Cross Reference or Substitution is being created.                                                                                                                                                                                                                                                | This will be used to identify the unique Cross Reference or Substitution record that will be updated.                                                                                                                                                                                                                                                  | This will be used to identify the unique Cross Reference or Substitution record that will be deleted from the System. Only values in this section will be used for a Delete.  All fields in the Main Body section will be ignored.                                                                            |
| From Part Number               | String         | Dependent    | 50         |    | This is the From Part Number that will be looked up on the Cross Reference record to determine which Substitution record to update.  The From Part Number and From Supplier fields must be populated.  If the From Part Number and From Supplier are passed in the Linkage Text doesn’t need to be passed in.                                          | This is the From Part Number that will be looked up on the Cross Reference record to determine which Substitution record to update.  The From Part Number and From Supplier fields must be populated.  If the From Part Number and From Supplier are passed in the Linkage Text doesn’t need to be passed in. |
| From Supplier                  | string         | Dependent    | 20         |    | This is the From Supplier the From Part Number will be looked up in.                                                                                                                                                                                                                                                                                   | This is the From Supplier the From Part Number will be looked up in.                                                                                                                                                                                                                                          |
| LinkageText                    | string         | Dependent    | 50         |    | This is the text value that will be used to look up a Cross Reference record to determine which Cross Reference record to update If this is populated the From Part Number and From Supplier fields don’t need to be passed in.                                                                                                                        | This is the text value that will be used to look up a Cross Reference record to determine which Cross Reference record to update If this is populated the From Part Number and From Supplier fields don’t need to be passed in.                                                                               |
| To Part Number                 | string         | Yes          | 50         |    | This is the To Part Number that will be looked up on the Cross Reference record to determine which Cross Reference or Substitution record to update.                                                                                                                                                                                                   | This is the To Part Number that will be looked up on the Cross Reference record to determine which Cross Reference or Substitution record to delete.                                                                                                                                                          |
| To Supplier                    | String         | Yes          | 20         |    | This is the Supplier the To Part Number will be looked up in.                                                                                                                                                                                                                                                                                          | This is the Supplier the To Part Number will be looked up in.                                                                                                                                                                                                                                                 |
| **Main Body**                  |    |  |      |    |  |   |
|  From Part Number              | String         | Dependent    | 50         | This is the From Part Number that the Substitution record will be created for. This must be a valid active Fusion Part Number. The From Part Number and From Supplier or Text field must be populated and if they are passed in the Linkage Text doesn’t need to be passed in.                                                         |  This is the From Part Number that will be updated on the Substitution record  from the looked up record in the Cross Reference Identity section. The From Part Number and From Supplier or Text field must be populated and if they are passed in the Linkage Text doesn’t need to be passed in.       This must be a valid active Fusion Part Number |   |
| From Supplier                  | String         | Dependent    | 20         | This is the Supplier the From Part Number will be looked up in.                                                                                                                                                                                                                                                                        | This is the Supplier the From Part Number will be looked up in.                                                                                                                                                                                                                                                                                        |   |
| LinkageText                    | String         | Dependent    | 50         | This is the Text Value that the Cross Reference will be created for.  If this is passed in the From Part Number and From Supplier fields don’t need to be passed in.                                                                                                                                                                   | This is the Text value that will be updated on the Cross Reference record from the looked up record in the Cross Reference Identity section. If this is passed in the From Part Number and From Supplier fields don’t need to be passed in.                                                                                                            |   |
| Customer Key                   | String         | Dependent    | 10         | This is the Fusion Customer Number that the Cross Reference applies to.  This field will be ignored if the From Part Number is populated, indicating this is a Substitution record being created.  If this is passed in the Branch is required as well.                                                                                | This is the Customer value that will be updated on the Cross Reference record from the looked up record in the Cross Reference Identity section.  This field will be ignored if the From Part Number is populated. If this is passed in the Branch is required as well.                                                                                |   |
| Branch                         | String         | Dependent    | 10         | This is the Customer Base Branch the Customer would be looked up in if the Customer value is passed in. if the Customer is passed in this would be required.                                                                                                                                                                           | This is the Customer Base Branch the Customer would be looked up in if the Customer value is passed in. if the Customer is passed in this would be required.                                                                                                                                                                                           |   |
| To Part Number                 | String         | Yes          | 50         | This is the To Part Number that Cross Reference or Substitution record is being created for.  This must be a valid active Fusion Part Number                                                                                                                                                                                           | This is the To Part Number value that will be updated on the Cross Reference or Substitution record from the looked up record in the Cross Reference Identity section. This must be a valid active Fusion Part Number                                                                                                                                  |   |
| To Supplier                    | String         | Yes          | 20         | This is the Supplier the To Part Number will be looked up in.                                                                                                                                                                                                                                                                          | This is the Supplier the To Part Number will be looked up in.                                                                                                                                                                                                                                                                                          |   |
| Cross Reference Message        | String         |  | 50         | This is the Cross Reference Message that will be used to display when looking at the Cross Reference or Substitution.  This must match a valid Cross Reference Message setup in Fusion.                                                                                                                                                | This is the Cross Reference Message value that will be updated on the Cross Reference or Substitution record from the looked up record in the Cross Reference Identity section.  This must be a valid Cross Reference Message setup in Fusion.                                                                                                         |   |
| Print Message on Invoice       | Boolean        |  | 1          | This is a field that indicates when the Cross Reference Message should print on the Invoice.  This will only apply to Cross References that are setup for a specific Customer.  A value of 1 should be passed in to set this to True, otherwise not including the field, blank value or 0 will indicate the value being set to False.  | This is the value of the Print Message Invoice checkbox that will be updated on the Cross Reference record from the looked up record in the Cross Reference Identity Section.  This will be ignored if the Cross Reference record being updated doesn’t have a Customer value populated.  This must either be 1 or 0 for Yes/No.                       |   |
| CreateReverseCR | Boolean        |  | 1          | This field will indicate whether to create a reverse Cross Reference from the To Part Number to the From Part Number.  This will only be used when creating a Record with the From Part Number populated.                                                                                                                              | This is the value of the Create Reverse Cross Reference checkbox that will be updated on the Cross Reference record from the looked up record in the Cross Reference Identity Section. This will be ignored if the record being updated doesn’t have a From Part Number populated. The must either be 1 or 0 for Yes or No                             |   |


### POST JSON Request Sample
```json
{

	"toPartNumber":"20576425",
	"toSupplier":"12345",
	"linkageText":"CR8",
	"CustomerKey":"1660",
	"Branch":"01",
	"crossReferenceMessage":"Cross Referenced with",
	"PrintOnInvoice":true  
}
```

### POST JSON Response Sample
```json
{
    "Status": "Cross Reference created successfully.",
    "Message": null
}
```

### PUT JSON Request Sample
```json
{
	"Identity":
	{
		"ToPartNumber":"0120689552",
		"Tosupplier":"MGU",
		"LinkageText":"0-120-689-552"
	},
	"ToPartNumber":"041585",
	"Tosupplier":"04K Test"
}
```

### PUT JSON Response Sample
```json
{
    "Status": "Cross Reference updated successfully.",
    "Message": null
}
```

### DELETE JSON Request Sample
```json
{
	"Identity":
	{
		"ToPartNumber":"007 993 40 01",
		"Tosupplier":"Q'STRAINTN",
		"LinkageText":"0079934001"
	}
}
```

### DELETE JSON Response Sample
```json
{
    "Status": "Cross Reference deleted successfully.",
    "Message": null
}
```
---
layout: post
title: "Create Parts Order"
category: "Parts" 
icon: "icon-gear"
type: "api" 
comments: false
description:  Create a parts order within Fusion and return an Order Number
---

---
---

The Part Order API is used to create a parts order 

When placing an order the parts and quantities passed to the API are processed as an order on the business system and, if successful, the order number is returned.  

**Validations for Part Order**

-   For customer with “On Hold” status in the business system, the order will be placed only if the “Allow order if On-Hold/Over Credit Limit?” flag is set to “Yes” for the customer in the Admin web site. Customer status is controlled by the business system.

---

#### Data Fields

| Name              | Max Length | Required | Description                                                                                                                                                                                                                                                                                      |
|-----------------------|----------------|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PartNum               | 50             | Y                             | Part Number business key from the business system. Must be the same value returned from the Part Search method for this part number.                                                                                                                                                                 |
| PartQuantity          | 11             | Y                             | Quantity to be ordered as a whole number.                                                                                                                                                                                                                                                            |
| PartPrice             | 11             |                               | The Price passed in can override the system pricing based on business system settings.                                                                                                                                                                                                               |
| ChargeName            | 50             | Y                             | Fusion only. The Miscellaneous Charge name exactly as it appears in Fusion.                                                                                                                                                                                                                          |
| ChargeQuantity        | 11             | Y                             | Fusion only. Quantity as a whole number.                                                                                                                                                                                                                                                             |
| ChargePrice           | 11             |                               | Fusion only. Price of the charge.                                                                                                                                                                                                                                                                    |
| ShippingSameAsBilling | 1              |                               | Flag to indicate if shipping information is same as billing information. Value ‘Y’ if yes and Value ‘N’ if not.                                                                                                                                                                                      |
| ShipToCompany Name    | 50             |                               | Same as Bill To Company Name if ShippingSameAsBilling flag is ‘Y’ and ShipToCompanyName is not blank. If blank then this will be provided by the business system. Similar to Retail Web site, an error message is returned if none of Company Name, ShipToFirstName and ShipToLastName are provided. |
| ShipToFirstName       | 50             |                               | Same as Bill To First Name if ShippingSameAsBilling is ‘Y and ShipToFirstName is not blank. If blank then this will be provided by the business system. Similar to Retail Web site, an error message is returned if none of Company Name, ShipToFirstName and ShipToLastName are provided.           |
| ShipToLastName        | 50             |                               | Same as Bill To Last Name if ShippingSameAsBilling flag is ‘Y’ and ShipToLastName is not blank. If blank then this will be provided by the business system. Similar to Retail Web site, an error message is returned if none of Company Name, ShipToFirstName and ShipToLastName are provided.       |
| ShipToAddressLine1    | 50             |                               | Optional if ShippingSameAsBilling flag is ‘Y’. The Ship to Address Line 1 is populated from Bill To Address Line 1 if ShipToAddressLine1 is not blank and ShippingSameAsBilling is ‘Y’. Mandatory if ShippingSameAsBilling is ‘N’ and ShipToAddressLine1 is blank.                                   |
| ShipToAddressLine2    | 50             |                               | If ShippingSameAsBilling flag is ‘Y’ and ShipToAddress Line 2 is blank then populate the Ship TO address line 2 with billing ship to address line 2.                                                                                                                                                 |
| ShipToCity            | 35             |                               | Optional if ShippingSameAsBilling flag is ‘Y’. If the ShipToCity is not provided and ShippingSameAsBilling is ‘N’ then ShipToCity is mandatory.                                                                                                                                                      |
| ShipToState           | 50             |                               | Optional if ShippingSameAsBilling flag is ‘Y’. If the ShipToState is blank and ShippingSameAsBilling is ‘N’ then ShipToState is mandatory.                                                                                                                                                           |
| ShipToPostal          | 15             |                               | Optional if ShippingSameAsBilling flag is ‘Y’. If the ShipToPostal is blank and ShippingSameAsBilling is ‘N’ then ShipToState is mandatory.                                                                                                                                                          |
| Phone                 | 20             |                               | If ShippingSameAsBilling flag is ‘Y’ and Phone is blank then populate the Phone with billing phone.                                                                                                                                                                                                  |
| CustomerComments      | 200            |                               | Comments/Shipping Instructions                                                                                                                                                                                                                                                                       |
| CustomerPONumber      | 20             |                               | If defined as required for the customer then this field is mandatory.                                                                                                                                                                                                                                |
| DeliveryMethod        | 100            |                               | DeliveryMethod must match a delivery method setup on the business system.                                                                                                                                                                                                                            |
| PaymentMethod         | 30             |                               | Fusion only. PaymentMethod must match a payment method setup on the business system.                                                                                                                                                                                                                 |

#### POST method
```json
{
  "Parts": [
	 {
		"PartNum": "7RPEF120",
		"PartQuantity": "10",
		"PartPrice": "25.00"
	 },
	 {
		"PartNum": "7RPEF120100",
		"PartQuantity": "1",
		"PartPrice": "0.50"
	 }
  ],
  "MiscCharges": [
	 {
		"ChargeName": "EPS/ShopM",
		"ChargeQuantity": "1",
		"ChargePrice": "20.00"
	 },
	 {
		"ChargeName": "misc",
		"ChargeQuantity": "2",
		"ChargePrice": "5.00"
	 },
  ],
  "ShippingSameAsBilling": "Y",
  "ShipToCompanyName": "ABC Distributors",
  "ShipToFirstName": "Business FName",
  "ShipToLastName": "Business LName",
  "ShipToAddressLine1": "1 Karmak Plaza",
  "ShipToAddressLine2": "",
  "ShipToCity": "Carlinville",
  "ShipToState": "ILLINOIS",
  "ShipToPostal": "62626",
  "Phone": "",
  "CustomerComments": "DELIVER TOMORROW",
  "CustomerPONumber": "JOE",
  "DeliveryMethod": "USPS",
  "PaymentMethod": ""
}
```

#### Sample Response
```json
{
   "Error": [],
   "Warning": [],
   "OrderNumber": "995374",
   "Message": []
}
```
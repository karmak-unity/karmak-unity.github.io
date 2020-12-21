---
layout: post
title: "Create Parts Order"
category: "Parts Sales Order"  
icon: "icon-gear"
type: "api" 
comments: false
description:  Create a parts order within Fusion and return an Order Number
---


The Part Order API is used to create a parts order.

When placing an order the parts and quantities passed to the API are processed as an order on the business system and, if successful, the order number is returned.


***NOTE: Requires Fusion version 3.60.10***
 
---
---

**Validations for Part Order**

- For customer with “On Hold” status in the business system, the order will be placed only if the “Allow order if On-Hold/Over Credit Limit?” flag is set to “Yes” for the customer in the Admin web site. Customer status is controlled by the business system.

---
---


#### Data Fields

| **Name**              | **Max Length** | **Required** | **Description**                                              |
| --------------------- | -------------- | ------------ | ------------------------------------------------------------ |
| LocationID     |     | Y | Branch or Location ID                                                                                                                                                                                         |
| DepartmentID   |     | Y | DepartmentID                                                                                                                                                                                                  |
| ID (Part)      | 50  | Y | PartsInventoryID as defined in the business system.                                                                                                                                                           |
| ID (Customer)  | 50  | Y | CustomerID as defined in the business system. Currently required to create a PartsSalesOrder, in the future it may be possible to find or create a customer by providing contact info in place of this field. |
| Quantity       | 11  | Y | Quantity to be ordered as a whole number.                                                                                                                                                                     |
| Price          | 11  | Y | Price that was collected for the part/charge.                                                                                                                                                                 |
| Name           | 50  | Y | Miscellaneous Charge name exactly as defined in the business system.                                                                                                                                          |
| CompanyName    | 50  |   |                                                                                                                                                                                                               |
| FirstName      | 50  |   |                                                                                                                                                                                                               |
| LastName       | 50  |   |                                                                                                                                                                                                               |
| AddressLine1   | 50  |   |                                                                                                                                                                                                               |
| AddressLine2   | 50  |   |                                                                                                                                                                                                               |
| City           | 35  |   |                                                                                                                                                                                                               |
| region         | 50  |   |                                                                                                                                                                                                               |
| Postal         | 15  |   |                                                                                                                                                                                                               |
| Phone          | 20  |   |                                                                                                                                                                                                               |
| Email          | 50  |   | May allow the DMS to send a copy of the invoice in the future.                                                                                                                                                |
| Comments       | 200 |   | Comments/Shipping Instructions                                                                                                                                                                                |
| OrderStatus    | 20  | Y | The Order Status generated by the API user. This provides a status to store in the FUSION system for the order  |
| PONumber       | 20  | Y | The Purchase Order number generated by the API user. This provides a reference to the invoice                                                                                                                 |
| DeliveryMethod | 100 | Y | DeliveryMethod must match a delivery method setup on the business system.                                                                                                                                     |
| PaymentMethod  | 30  | Y | PaymentMethod must match a payment method setup on the business system.                                                                                                                                       |
 
 


#### REQUEST POST URL
```
.../unityapi/PartOrder
```


#### POST method
```json
{
	"locationID": "2345644",
	"departmentID": "4",
	"comments": "DELIVER TOMORROW",
	"Parts": [
		{
			"ID": "7RPEF120",
			"quantity": "10",
			"price": "25.00"
		},
		{
			"ID": "7RPEF120100",
			"Quantity": "1",
			"Price": "0.50"
		}
	],
	"miscCharges": [
		{
			"Name": "EPS/ShopM",
			"Quantity": "1",
			"Price": "20.00"
		},
		{
			"Name": "Shipping",
			"Quantity": "2",
			"Price": "5.00"
		},
	],
	"Customer": {
		"ID": ""
	},
	"Shipping": {
		"ShippingSameAsBilling": "Y",
		"companyName": "ABC Distributors",
		"firstName": "Business FName",
		"lastName": "Business LName",
		"addressLine1": "1 Karmak Plaza",
		"addressLine2": "",
		"city": "Carlinville",
		"region": "IL",
		"postal": "62626",
		"phone": "222-222-2222",
		"DeliveryMethod": "USPS",
	},
	"Payment": {
		"OrderStatus": "Paid",
		"PONumber": "13DB876973",
		"PaymentMethod": "VISA"
	}
}
```

#### Sample Response
```json
{
    "locationID": "1",
    "departmentID": "1",
    "orderNumber": "200645",
    "customerID": "1487",
    "orderTotal": "-4.2900",
    "lineItems": [
        {
            "partNumber": "0218GG151-C",
            "supplier": "Bendix",
            "description": "Exchange Part -Core",
            "type": "RET",
            "action": "Sale",
            "quantity": "-1",
            "price": "4.2940",
            "extendedPrice": "-4.2900"
        }
    ],
    "messages": [
        "success"
    ]
}
```
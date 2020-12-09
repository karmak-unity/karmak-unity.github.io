---
layout: post  
title: "Parts Search and Availability"  
category: "Parts Sales Order"  
icon: "icon-gear"  
type: "api"  
comments: false  
description: Allow user to search for parts by part ID, Description and by part Supplier (Manufacturer)
---


The Part Search API is used to search for parts by part ID, Description and by part Supplier (Manufacturer)

The Search returns detail part information including pricing by customer if requested and quantity available.



***NOTE: Requires Fusion version 3.60.10***

---
---

### Request Fields

| Name            |  Length  | Required |      | Description                                                             |
| ----------- | -------- | ---- | ------------------------------------------------------------ |
| locationID  |          | Y    | Location or Branch ID                                        |
| customerID  | 20       |      | unique customer Identifier within Fusion system              |
| region      | 6        |      | State / region / area                                        |
| number      | 30       | O*   | Part Number to be searched for. *If Part Description field is set then this is optional. |
| description | 50       | O*   | Description for part to be searched for. *If Part Number field is set then this is optional. |
| exactMatch  | boolean1 |      | Flag for returning only exact matches. If set to true, only parts that match the search criteria exactly will be returned. Default is TRUE |
| source      | 10       |      | The source or Supplier of the part to be searched for.       |


#### Business Logic

| exactMatch | number | description | result |
|-----------------|-----------------|----------------|--------------------------------------------------------------------------------------|
| true            | has value       | blank          | return exact part match using number, description is ignored in search               |
| true            | has value       | has value      | return exact part match using number AND description                                 |
| true            | blank           | has value      | return exact part match using description, name is ignored in search                 |
| true (or) false | blank           | blank          | error returned / missing a required filed                                            |
| false           | has value \>= 5 | less than 5    | return part match list using number with wildcard, description is ignored in search  |
| false           | has value \>=5  | has value \>=5 | return part match list using number AND description with wildcards on each           |
| false           | less than 5     | has value \>=5 | return part match list using description with wildcards, number is ignored in search |
| false           | less than 5     | less than 5    | error returned / minimum length not submitted in a required filed                    |

### Response Fields

| Name | Length | Description |
|--------------|----|--------------------------------------------------------|
| number       | 30 | Business system part number                            |
| description  | 50 | Business system part description                       |
| supplierCode | 6  | Business system supplier code                          |
| ID           | 4  | Business system unique product code                    |
| weight       | 13 | Business system weight per part                        |
| available    | 12 | Part’s current quantity on hand or availability status |
| price        | 12 | Customer’s calculated price for part                   |
| listPrice    | 12 | Business system part list price                        |
| EHCCharge    | 12 | Environmental handling charges associate with the part |

---
---

## Part Search 

### POST 
```
/api/unity/{version}/unityapi/PartsSearch/Search
```


### REQUEST
```json
[
{
	"customerID": "bu4999",
	"locationID": "234234",
	"parts": [
		{
			"number": "F120",
			"description": "F120",
			"exactMatch": false,
			"source": ""
		},
		{
			"number": "F121",
			"description": "F121",
			"exactMatch": false,
			"source": ""
		}
	]
}
]
```


#### RESPONSE
```json
[

    {
	"criteria": {
		"number": "F120",
        "description": "F120",
        "exactMatch": false,
        "source": ""
	},
	"results": [
		{
			"ID": "4387hgj9",
			"number": "F120",
			"description": "Diamond Encrusted Dinglehopper",
			"SupplierCode": "1232",
			"Weight": "8",
			"Available": "24",
			"Price": {
				"customerPrice": "8.00",
				"listPrice": "12.00"
			},
			"Core": {
				"Number": "",
				"Description": "",
				"Price": "",
				"EHCCharge": ""
				}
		},
		{
			"ID": "4387hffs9",
			"number": "F120233",
			"Description": "Diamond Encrusted Dinglehopper",
			"SupplierCode": "1235",
			"Weight": "8",
			"Available": "12",
			"Price": {
				"customerPrice": "9.00",
				"listPrice": "0.00"
			},
			"Core": {
				"Number": "",
				"Description": "",
				"Price": "",
				"EHCCharge": ""
				}
		}],
	"message" : ""
	},
    {
		"criteria": {
		    "number": "F121",
            "description": "F121",
            "exactMatch": false,
            "source": ""
		},
		"results": [
		{
			"ID": "2000sdf34",
			"number": "F121ddd",			
			"Description": "Snifflewaffle",
			"SupplierCode": "1232",
			"Weight": "12",
			"Available": "2",
			"Price": {
				"customerPrice": "676.00",
				"listPrice": "714.00"
			},
			"Core": {
				"Number": "",
				"Description": "",
				"Price": "",
				"EHCCharge": ""
			}
		}
		],
		"message" : ""
	}
]
```


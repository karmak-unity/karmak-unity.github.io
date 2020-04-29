---
layout: post
title: "Data Access via API"
category: "Data Access Documentation"
type: "usage" 
comments: false
description: How to access and format the request
---
The Data Access API suite exposes self-service reporting views via Unity APIs. 
---
---

### Operations
---
The Data Access API suite exposes GET requests.

---
---

### Routing/URL
---

Unity handles all requests through a single endpoint.
```
https://api.karmak.io/api/unity/{version}/unityapi/frw/{viewname}?{*parameters*}
```

### Usage 
**Version**: API Version; v1 as of June 30, 2019

**Viewname**: the viewname field is identified by the "Key" property in Data Field Properties file (version specific).

**Parameters**: Parameters are further defined below in sections Filtering, Sorting, and Pagination

---
---

### Filtering
---
Filters (WHERE criteria) are specified as querystring parameters.
-   Filter values and column names that contain spaces or special characters
    must be URL encoded.
-   The filter parameter is only specified once for either a single filter
    criteria or multiple.
-   When multiple filter criteria is used, parameters should be separated by
    commas.
-   If call contains multiple filter criteria, they will be joined via "AND."
-   When using the IN operator, selection criteria is pipe "\|" separated.
```
{columnname}[{operation}]{criteria}
```

### Operations

|---|---|
| EQ  | Equals                   |
| LT  | Less Than                |
| LTE | Less Than or Equal To    |
| GT  | Greater Than             |
| GTE | Greater Than or Equal To |
| NE  | Not Equal To             |
| IN  | In                       |

**Example Parameters**

| Parameter | Description |
|---|---|
|filter=invoice_id[EQ]123456 | for results where Invoice ID  123456 |
|filter=invoice_id[LTE]123456,invoice_status[EQ]open | for results where Invoice ID \< 123456, and Invoice Status  Open|
|filter=invoice_date[GT]01-01-2019,invoice_status[IN]paid\|posted |for results where Invoice Date \> 01/01/2019, and Invoice Status is either Paid or Posted|


---
---

### Sorting
---
The sort parameter is only specified once, for either single or multiple
columns.  When multiple sort criteria is used, parameters should be separated by
commas.
-   Default sort order  ASCENDING. 
-   To change sort order to DESCENDING, precede column name with **-** (minus
    sign).
```
sort={order}{columnname},{order}{columnname}
```
**Example Parameters**

| Parameter | Description |
|---|---|
|sort=invoice_id |to sort results in ASCENDING order by Invoice ID|
|sort=-invoice_status,-invoice_id | to sort results in DESCENDING order by Invoice Status, then DESCENDING order by Invoice ID|


---
---

### Selecting
---
The select parameter is used for accessing a specified subset of columns in a data view. The subset list of desired columns is delimited by a comma.
```
select={columnname},{columnname},{columnname}
```

**Example Parameters**

| Parameter                        | Description                                                  |
| -------------------------------- | ------------------------------------------------------------ |
| select=UserName                  | would return a data set with exclusively username fields             |
| select=UserName,FirstName,LastName | would return a data set with UserName, FirstName, and LastName fields |

---

**Conflicts with Sorting**

When using the sort parameter, it is important to make sure each sort column is selected. If a sort column is not included in the select parameter the request will fail.
-	EX: select=UserName&sort=UserId Will fail!
-	EX: select=UserName,FirstName,LastName&sort=UserId,AddDate Will fail!
-	EX: select=UserName,FirstName,LastName&sort=UserId,LastName Will fail!
-	EX: select=UserName,UserId&sort=UserId Will pass!
-	EX: select=UserName,UserId,LastName&sort=UserId,UserName Will pass!

**Automatic Sort Behavior**

Data sets have a default sort column pre-defined.  When using the Select parameter and NOT using the sort parameter, the data will either be sorted using the pre-defined default sort (if it is included in the Select parameter) or the first column provided in the Select parameter.

---
---

### Pagination
---
Paging of the result set is handled by specifying page size and page number in
the request.
-   Page numbering begins at 1.
-   Requests for a page beyond the available data will return an empty result.
-   Each view defines maximum page size (in Unity View Properties, attached).  Requests greater than maximum page size will revert to maximum page size when results are returned.
	
```
page={pagenumber}&pagesize{pagesize}
```

**Example Parameters**

| Parameter | Description |
|---|---|
|page=1&pagesize=100 | start at page 1 and return 100 results |
|page=12&pagesize=500| start at page 12 and return 500 results |



---
---

### Aliasing

---

Aliasing can be used to rename the columns received from Unity. Simply select a column and provide a new name in the following format:
 select={columnname}:{newname}

It is possible to use more than one alias at a time:

select={columnname}:{newname},{columnname}:{newname},{columnname}:{newname}


**Examples**

select=UserName  and with alias: select=UserName:User
```json
[
	{ "UserName": "MyUser"},
    { "UserName": "MyUser2"}
]

[
	{ "User": "MyUser"},
	{ "User": "MyUser2"}
]
```
select=UserName:User,UserNumber:Id,DOB:Birthday
```json
[
	{ 
        "User": "MyUser"
        "ID": "1"
        "Birthday": "03-02-1973"
    },
    {
    	"User": "MyUser2"
        "ID": "2"
        "Birthday": "01-21-1985"
    }
]
```
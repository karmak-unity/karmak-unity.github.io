---
layout: post
title: "Data Access via API"
category: "Documentation"
type: "usage" comments: falsedescription: Exposes self-service reporting views via Unity APIs
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

>   https://api.karmak.io/api/unity/{version}/unityapi/frw/{viewname}?{*parameters*}

-   Version  API Version; v1 as of June 30, 2019

-   View  View Key, as defined in Unity View Properties (attached)

-   Parameters  further defined below in sections Filtering, Sorting,
    Pagination

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

>   {columnname}[{operation}]{criteria}

>   **Operations**

| EQ  | Equals                   |
|---|---|
| LT  | Less Than                |
| LTE | Less Than or Equal To    |
| GT  | Greater Than             |
| GTE | Greater Than or Equal To |
| NE  | Not Equal To             |
| IN  | In                       |

Example Parameters

>   filterinvoice_id[EQ]123456 (for results where Invoice ID  123456)

>   filterinvoice_id[LTE]123456,invoice_status[EQ]open (for results where
>   Invoice ID \< 123456, and Invoice Status  Open)

>   filterinvoice_date[GT]01-01-2019,invoice_status[IN]paid\|posted (for
>   results where Invoice Date \> 01/01/2019, and Invoice Status is either Paid
>   or Posted)

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

>   sort{order}{columnname},{order}{columnname}

Example Parameters

>   sortinvoice_id (to sort results in ASCENDING order by Invoice ID)

>   sort-invoice_status,-invoice_id (to sort results in DESCENDING order by
>   Invoice Status, then DESCENDING order by Invoice ID)

---
---
### Pagination
---

Paging of the result set is handled by specifying page size and page number in
the request.

-   Page numbering begins at 1.

-   Requests for a page beyond the available data will return an empty result.

-   Each view defines maximum page size (in Unity View Properties, attached). 
    Requests greater than maximum page size will revert to maximum page size
    when results are returned.

>   page{pagenumber}&pagesize{pagesize}

Example Parameters

>   page1&pagesize100

>   page12&pagesize500

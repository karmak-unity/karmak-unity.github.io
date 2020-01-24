---
layout: post
title: "Data Field Properties"
icon: "icon-list-alt"
category: "Data Access Documentation"
type: "usage" comments: falsedescription: Data reference documentation for fields, field types, and size
---

---
The Report DataAccess API suite exposes GET requests to the Fusion DMS. The properties may vary by version. Control fields are listed at the beginning of each property set. 
---
### Field Properties

#### Key 
This is the external name which will be used in a Unity API call.

#### Type
This helps determine what type the underlying functionality is such as "View" for the SQL SSR views.
#### HasReturn
This is a True/False indicator to show if the underlying functionality has return data for example from an RPC call.
#### ReturnType
This describes the data type of the return data for example from an RPC call.
#### DefaultSort
This determines the default sorting to use if one is not provided in the Unity call for example the output from calling a SQL SSR view.
#### DefaultPageSize
This is the number of rows to return if no page size was provided in the Unity call.
#### MaxPageSize
This is the maximum number of rows that can be returned in the Unity call.
#### Input
This is a list of the input variables to be used, each entry has a property for the name and data type.
#### Output
This is a list of the output variables provided, each entry has a property for the name and data type.
------
<p class= "catheader"> Fusion Version Specific Data Properties</p>
Click the version(s) below to see version specific properties
{% assign sorted-posts = site.posts | where: "category", "Fusion Version Data Properties" | sort: 'title' %}
{% for post in sorted-posts limit:200 %}
<h5> <a href="{{ site.baseurl}}{{ post.url }}.html"  onclick="window.open(this.href,'_new','addressbar=no,toolbar=no,location=no,status=no,menubar=no,scrollbars=yes,resizable=no,width=700,height=550'); return false;">{{ post.title }}</a></h5>
{% endfor %}
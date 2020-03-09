---
layout: post
title: "Accounting Comments"
category: "Accounting Other" 
icon: "icon-credit-card1"
type: "data_access" comments: falsedescription: Access the comments from the Comments Tabs located on multiple forms within Fusion
---


---

This data object will display comments from the Comments Tab that is located on
multiple forms in the Fusion Application.  The user will be able to join between
the Source Data Object and the Comment Data Object.  At this time this Data
Object will only display Comments from the Customer Record until Fusion Report
Writer is updated to have more joins from other forms that store comments.

 <!-- 


 -->  <hr>Field Details...

| **SQL Field Name**      | **Column Description**                                                                                                                                           |
|---|---|
| AddDate                 | This is the date the comment was added in Fusion.                                                                                                                |
| AddUser                 | This is the user that added the comment in Fusion.                                                                                                               |
| BriefDescription        | This is the Brief Description of the Comment that was entered.                                                                                                   |
| Comment                 | This is the actual comment that the user entered in Fusion.                                                                                                      |
| CommentTable            | This is the Comment Table that the comment is associated with.  This will explain what Fusion form the comment is associated with, such as Customer, Unit, etc…. |
| CommentTableDescription | This is the Description of the Comment Table.                                                                                                                    |
| CommentType             | This is the comment type that is associated with the comment that the user entered.                                                                              |
| CommentTypeDescription  | This is the description of the comment type.                                                                                                                     |
| LastUpdate              | This is the date the comment was last updated in Fusion.                                                                                                         |
| UpdateUser              | This is the user that last updated the comment in Fusion.                                                                                                        |
| Posted                  | This is a flag that will show if the comment was a Technician Story whether or not it was posted to the Repair Order.                                            |
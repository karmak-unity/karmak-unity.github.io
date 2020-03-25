---
layout: post
title: "Velocity Codes"
category: "Helper APIs" 
icon: "icon-question1"
type: "data_access"comments: falsedescription: Allow the user to pull back Velocity Codes, to be used in support of the Customer Special Pricing API
---

---

The Velocity Code Type API is a GET method API that will allow the user to pull back Velocity Codes, to be used in support of the Customer Special Pricing API, to create Velocity pricing records.

---
Field Details...

| Field           | Definition |
|---|---|
| VelocityCodeTypeID | Unique database ID for the velocity code type. |
| VelocityCodeType   | Velocity code type                                                                       |
| Description        | Velocity code type description                                                           |
| Inactive           | When set to TRUE, the velocity code type is inactive (no longer used or valid for entry) |
| AddUserID          | Unique database ID of the user that added the record                                     |
| AddUser            | User that added the record                                                               |
| AddDate            | Date the record was added                                                                |
| UpdateUserID       | Unique database ID of the user that last updated the record                              |
| LastUpdateUser     | User that last updated the record                                                        |
| LastUpdateDate     | Date the record was last updated                                                         |

---
title: POST List/TicketStatus/Items
id: v1TicketStatusList_PostTicketStatusEntity
---

# POST List/TicketStatus/Items

```http
POST /api/v1/List/TicketStatus/Items
```

Create a new TicketStatusEntity list item

Calls the List agent service SaveTicketStatusEntity.






## Request Headers

| Parameter Name | Description |
|----------------|-------------|
| Authorization  | Supports 'Basic', 'SoTicket' and 'Bearer' schemes, depending on installation type. |
| X-XSRF-TOKEN   | If not using Authorization header, you must provide XSRF value from cookie or hidden input field |
| Content-Type | Content-type of the request body: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept         | Content-type(s) you would like the response in: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept-Language | Convert string references and multi-language values into a specified language (iso2) code. |
| SO-Language | Convert string references and multi-language values into a specified language (iso2) code. Overrides Accept-Language value. |
| SO-Culture | Number, date formatting in a specified culture (iso2 language) code. Partially overrides SO-Language/Accept-Language value. Ignored if no Language set. |
| SO-TimeZone | Specify the timezone code that you would like date/time responses converted to. |
| SO-AppToken | The application token that identifies the partner app. Used when calling Online WebAPI from a server. |

## Request Body: newEntity  

The TicketStatusEntity to be created. 

| Property Name | Type |  Description |
|----------------|------|--------------|
| TicketStatusId | int32 | The primary key (auto-incremented) |
| Name | string | Name of user defined ticket status |
| Status | string | The &amp;apos;classic&amp;apos; ticket status. I.e. active/closed/postponed/deleted |
| TimeCounter | string | Which field in ticket we count time spent on (queue, internal, external) |
| NoEmailReopen | bool | Whether inbound emails can reopen requests with this status or not |
| IsDefault | bool | Indicates if status is default one as there might be more than one status with same internal status |
| UsedInQueue | bool | If set, status is used in GetNext calculations |


## Response: object

Entity for a ticket status. This entity describes the meta data for a ticket status, and provides special operations on it.



Carrier object for TicketStatusEntity.
Services for the TicketStatusEntity Carrier is available from the <see cref="T:SuperOffice.CRM.Services.IListAgent">List Agent</see>.

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body: object

| Property Name | Type |  Description |
|----------------|------|--------------|
| TicketStatusId | int32 | The primary key (auto-incremented) |
| Name | string | Name of user defined ticket status |
| Status | string | The &amp;apos;classic&amp;apos; ticket status. I.e. active/closed/postponed/deleted |
| TimeCounter | string | Which field in ticket we count time spent on (queue, internal, external) |
| NoEmailReopen | bool | Whether inbound emails can reopen requests with this status or not |
| IsDefault | bool | Indicates if status is default one as there might be more than one status with same internal status |
| UsedInQueue | bool | If set, status is used in GetNext calculations |
| TableRight |  |  |
| FieldProperties | object |  |

## Sample Request

```http!
POST /api/v1/List/TicketStatus/Items
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

{
  "TicketStatusId": 619,
  "Name": "Nolan-Morissette",
  "Status": "Active",
  "TimeCounter": "Externally",
  "NoEmailReopen": true,
  "IsDefault": false,
  "UsedInQueue": true
}
```

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "TicketStatusId": 532,
  "Name": "Torphy Inc and Sons",
  "Status": "Active",
  "TimeCounter": "Externally",
  "NoEmailReopen": false,
  "IsDefault": false,
  "UsedInQueue": true,
  "TableRight": {
    "Mask": "Delete",
    "Reason": ""
  },
  "FieldProperties": {
    "fieldName": {
      "FieldRight": {
        "Mask": "FULL",
        "Reason": ""
      },
      "FieldType": "System.Int32",
      "FieldLength": 892
    }
  }
}
```
---
title: PUT List/ProjectType/Headings
uid: v1ProjectTypeList_PutProjectTypeHeadings
---

# PUT List/ProjectType/Headings

```http
PUT /api/v1/List/ProjectType/Headings
```

Saves headings for the ProjectType list.


Calls the List agent service SaveHeadingsFromListDefinition.







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

## Request Body: entities 

The headings to be saved. 

| Property Name | Type |  Description |
|----------------|------|--------------|
| HeadingId | Integer | Primary key |
| Name | String | The visible heading |
| Tooltip | String | Tooltip or other description |
| Deleted | Boolean | True if the heading is marked as deleted |
| Rank | Integer | Rank order |
| UdListDefinitionId | Integer | The id of the list which this heading belongs to |

## Response:array

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: array

| Property Name | Type |  Description |
|----------------|------|--------------|
| HeadingId | int32 | Primary key |
| Name | string | The visible heading |
| Tooltip | string | Tooltip or other description |
| Deleted | bool | True if the heading is marked as deleted |
| Rank | int32 | Rank order |
| UdListDefinitionId | int32 | The id of the list which this heading belongs to |
| TableRight | RecurrenceInfo |  |
| FieldProperties | object |  |

## Sample request

```http!
PUT /api/v1/List/ProjectType/Headings
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

[
  {
    "HeadingId": 637,
    "Name": "McKenzie Inc and Sons",
    "Tooltip": "ut",
    "Deleted": false,
    "Rank": 244,
    "UdListDefinitionId": 176
  },
  {
    "HeadingId": 637,
    "Name": "McKenzie Inc and Sons",
    "Tooltip": "ut",
    "Deleted": false,
    "Rank": 244,
    "UdListDefinitionId": 176
  }
]
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "HeadingId": 141,
    "Name": "Ryan, Corwin and Rice",
    "Tooltip": "alias",
    "Deleted": false,
    "Rank": 7,
    "UdListDefinitionId": 703,
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.Int32",
        "FieldLength": 694
      }
    }
  }
]
```
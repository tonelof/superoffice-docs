---
title: POST Agents/EMail/GetMailFromInReplyTo
uid: v1EMailAgent_GetMailFromInReplyTo
---

# POST Agents/EMail/GetMailFromInReplyTo

```http
POST /api/v1/Agents/EMail/GetMailFromInReplyTo
```

Get email from db based on In-Reply-To Message Id


## Online Restricted: ## The EMail agent is not available in Online by default. Access must be requested specifically when app is registered.






## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category". Default = show all fields. |

```http
POST /api/v1/Agents/EMail/GetMailFromInReplyTo?$select=name,department,category/id
```


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

## Request Body: request 

MessageId 

| Property Name | Type |  Description |
|----------------|------|--------------|
| MessageId | String |  |

## Response:

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: EMailEntity

| Property Name | Type |  Description |
|----------------|------|--------------|
| To | array | To recipients of e-mail |
| Cc | array | Cc recipients of e-mail |
| Bcc | array | Bcc recipient of e-mail |
| Subject | string | Subject of the e-mail |
| HTMLBody | string | Body formatted in HTML |
| From | EMailAddress | Who did the e-mail originate from |
| Sent | date-time | When was the e-mail sent |
| Size | int32 | Total size of the e-mail |
| Priority | string | Importance of the e-mail |
| Flags | string | Flag status of this mail (unread, replied, deleted ) |
| MessageID | string | Unique id of e-mails |
| PlainBody | string | Body formatted in plain text |
| IsSent | bool | Is this a sent e-mail (not new) |
| EMailSOInfo | EMailSOInfo | Glue between SuperOffice data and an e-mail. |
| ServerId | int32 | Unique id for the e-mail on the server |
| Attachments | array |  |
| CustomHeaderList | array | Non standard e-mail headers |
| FolderName | string | Name of folder the e-mail belongs in |
| EmailItemId | int32 | Primary key |
| AccountId | int32 | Account Id |
| ReceivedAt | date-time | Received date time |
| InReplyTo | EMailEnvelope | The envelope of the email this email is a reply to, if it exists |
| RepliedAt | date-time | When this email was replied at |
| HasCalendarData | bool | If this email contains exactly one iCal appointment |
| CalMethod | string | Method stored in the associated iCal appointment. Indicates if the iCal data is a reply, counter proposal etc. |
| CalReplyStatus | string | Reply status stored in calendar data for the ical method is REPLY |
| TableRight | TableRight |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/EMail/GetMailFromInReplyTo
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

{
  "MessageId": "maxime"
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "To": [
    {
      "ContactId": 615,
      "ContactName": "Cormier-Boyer",
      "PersonId": 317,
      "PersonName": "Morar-Brakus",
      "AssociateId": 165,
      "Address": "ut",
      "EmailId": 474,
      "DuplicatePersonIds": [
        198,
        275
      ],
      "Name": "Hackett Inc and Sons",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 414
        }
      }
    }
  ],
  "Cc": [
    {
      "ContactId": 349,
      "ContactName": "Vandervort Group",
      "PersonId": 240,
      "PersonName": "Schinner, Koepp and Weimann",
      "AssociateId": 523,
      "Address": "natus",
      "EmailId": 52,
      "DuplicatePersonIds": [
        956,
        895
      ],
      "Name": "Schimmel Group",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 368
        }
      }
    }
  ],
  "Bcc": [
    {
      "ContactId": 470,
      "ContactName": "Huel-Kovacek",
      "PersonId": 725,
      "PersonName": "Kuhic LLC",
      "AssociateId": 865,
      "Address": "quaerat",
      "EmailId": 580,
      "DuplicatePersonIds": [
        568,
        915
      ],
      "Name": "Terry LLC",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 923
        }
      }
    }
  ],
  "Subject": "et",
  "HTMLBody": "voluptas",
  "From": null,
  "Sent": "2016-08-15T17:37:17.8752432+02:00",
  "Size": 337,
  "Priority": "High",
  "Flags": "Answered",
  "MessageID": "iusto",
  "PlainBody": "cumque",
  "IsSent": false,
  "EMailSOInfo": null,
  "ServerId": 853,
  "Attachments": [
    {
      "Description": "Mandatory mission-critical groupware",
      "Filename": "eos",
      "Size": 520,
      "Type": "nesciunt",
      "Encoding": "eum",
      "Id": "est",
      "Disposition": "quis",
      "Stream": "GIF89....File contents as raw bytes...",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 233
        }
      }
    }
  ],
  "CustomHeaderList": [
    {
      "Name": "Olson, Ebert and Heaney",
      "Values": [
        "exercitationem",
        "sit"
      ],
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 244
        }
      }
    },
    {
      "Name": "Olson, Ebert and Heaney",
      "Values": [
        "exercitationem",
        "sit"
      ],
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 244
        }
      }
    }
  ],
  "FolderName": "Schimmel, Doyle and Carroll",
  "EmailItemId": 630,
  "AccountId": 619,
  "ReceivedAt": "2020-12-04T17:37:17.8762411+01:00",
  "InReplyTo": null,
  "RepliedAt": "2021-05-04T17:37:17.8762411+02:00",
  "HasCalendarData": false,
  "CalMethod": "Add",
  "CalReplyStatus": "Accepted",
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 82
    }
  }
}
```
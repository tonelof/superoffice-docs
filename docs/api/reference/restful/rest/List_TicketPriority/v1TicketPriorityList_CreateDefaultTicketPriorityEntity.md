---
title: GET List/TicketPriority/Items/Default
id: v1TicketPriorityList_CreateDefaultTicketPriorityEntity
---

# GET List/TicketPriority/Items/Default

```http
GET /api/v1/List/TicketPriority/Items/Default
```

Gets a default TicketPriorityEntity list item.








## Request Headers

| Parameter Name | Description |
|----------------|-------------|
| Authorization  | Supports 'Basic', 'SoTicket' and 'Bearer' schemes, depending on installation type. |
| X-XSRF-TOKEN   | If not using Authorization header, you must provide XSRF value from cookie or hidden input field |
| Accept         | Content-type(s) you would like the response in: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept-Language | Convert string references and multi-language values into a specified language (iso2) code. |
| SO-Language | Convert string references and multi-language values into a specified language (iso2) code. Overrides Accept-Language value. |
| SO-Culture | Number, date formatting in a specified culture (iso2 language) code. Partially overrides SO-Language/Accept-Language value. Ignored if no Language set. |
| SO-TimeZone | Specify the timezone code that you would like date/time responses converted to. |
| SO-AppToken | The application token that identifies the partner app. Used when calling Online WebAPI from a server. |


## Response: object

Entity for a ticket priority. This entity describes the meta data for a ticket priority, and provides special operations on it.



Carrier object for TicketPriorityEntity.
Services for the TicketPriorityEntity Carrier is available from the <see cref="T:SuperOffice.CRM.Services.IListAgent">List Agent</see>.

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body: object

| Property Name | Type |  Description |
|----------------|------|--------------|
| TicketPriorityId | int32 | The primary key (auto-incremented) |
| Name | string | The name of the priority. |
| Status | string | The status (normal/deleted) of the priority. |
| Flags | string | A bitmask of flags. |
| SortOrder | int32 | Indicates the sort order for this priority. 1 is first, 100 is last |
| TicketRead | string | This field indicates what to do with the escalation chain when the request is read |
| ChangedOwner | string | This field indicates what to do with the escalation chain when the request changes owner (manually) |
| TicketNewinfo | string | This field indicates what to do with the escalation chain when the request gets new info |
| TicketClosed | string | This field indicates what to do with the escalation chain when the request is closed |
| TicketChangedPriority | string | This field indicates what to do with the escalation chain when the request is changed into this priority |
| TicketNew | string | This field indicates what to do with the escalation chain when a new request is registered |
| Deadline | int32 | Deadline to add if escalated (minutes) |
| MonStart | date-time | The work hour start for Mondays. Note that only the time part of the DateTime is used |
| MonStop | date-time | The work hour start for Mondays. Note that only the time part of the DateTime is used |
| TueStart | date-time | The work hour start for Tuesdays. Note that only the time part of the DateTime is used |
| TueStop | date-time | The work hour stop for Tuesdays. Note that only the time part of the DateTime is used |
| WedStart | date-time | The work hour start for Wednesdays. Note that only the time part of the DateTime is used |
| WedStop | date-time | The work hour stop for Wednesdays. Note that only the time part of the DateTime is used |
| ThuStart | date-time | The work hour start for Thursdays. Note that only the time part of the DateTime is used |
| ThuStop | date-time | The work hour stop for Thursdays. Note that only the time part of the DateTime is used |
| FriStart | date-time | The work hour start for Fridays. Note that only the time part of the DateTime is used |
| FriStop | date-time | The work hour stop for Fridays. Note that only the time part of the DateTime is used |
| SatStart | date-time | The work hour start for Saturdays. Note that only the time part of the DateTime is used |
| SatStop | date-time | The work hour stop for Saturdays. Note that only the time part of the DateTime is used |
| SunStart | date-time | The work hour start for Sundays. Note that only the time part of the DateTime is used |
| SunStop | date-time | The work hour stop for Sundays. Note that only the time part of the DateTime is used |
| NonDates | array | Dates which the escalation time should not be running. Note that only the day of the year (day and month) is used. So the year and time part is not used even if this is a DateTime |
| EscalationLevels | array | Escalation levels bound to the parent priority |
| TableRight |  |  |
| FieldProperties | object |  |

## Sample Request

```http!
GET /api/v1/List/TicketPriority/Items/Default
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: *
```

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "TicketPriorityId": 592,
  "Name": "Kerluke, Tremblay and Wehner",
  "Status": "Deleted",
  "Flags": "AlertSchedule",
  "SortOrder": 329,
  "TicketRead": "Continue",
  "ChangedOwner": "Continue",
  "TicketNewinfo": "Continue",
  "TicketClosed": "Continue",
  "TicketChangedPriority": "Continue",
  "TicketNew": "Continue",
  "Deadline": 849,
  "MonStart": "2012-07-26T18:25:52.309673+02:00",
  "MonStop": "2019-04-14T18:25:52.309673+02:00",
  "TueStart": "2005-07-25T18:25:52.309673+02:00",
  "TueStop": "2012-10-13T18:25:52.309673+02:00",
  "WedStart": "1997-10-21T18:25:52.309673+02:00",
  "WedStop": "2008-02-27T18:25:52.309673+01:00",
  "ThuStart": "2021-01-09T18:25:52.309673+01:00",
  "ThuStop": "1997-12-24T18:25:52.309673+01:00",
  "FriStart": "2004-07-25T18:25:52.309673+02:00",
  "FriStop": "2007-09-21T18:25:52.309673+02:00",
  "SatStart": "2005-07-04T18:25:52.309673+02:00",
  "SatStop": "1999-06-07T18:25:52.309673+02:00",
  "SunStart": "1997-01-03T18:25:52.309673+01:00",
  "SunStop": "2007-06-14T18:25:52.309673+02:00",
  "NonDates": [
    "sed",
    "optio"
  ],
  "EscalationLevels": [
    {
      "TicketAlertId": 517,
      "AlertLevel": 923,
      "AlertTimeout": 558,
      "Action": 573,
      "DelegateTo": 764,
      "ScriptId": 870,
      "EmailTo": "delaney.wilkinson@bartellkoch.ca",
      "SmsTo": "iste",
      "ReplyTemplateIdCustomer": 325,
      "ReplyTemplateIdUser": 107,
      "ReplyTemplateIdCatmast": 586,
      "ReplyTemplateIdEmail": 48,
      "RtiCustomerSms": 142,
      "ReplyTemplateIdUserSms": 976,
      "ReplyTemplateIdCatmastSms": 561,
      "ReplyTemplateIdSms": 949,
      "TableRight": {},
      "FieldProperties": {
        "fieldName": {
          "FieldRight": {
            "Mask": "FULL",
            "Reason": ""
          },
          "FieldType": "System.Int32",
          "FieldLength": 880
        }
      }
    }
  ],
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
      "FieldLength": 766
    }
  }
}
```
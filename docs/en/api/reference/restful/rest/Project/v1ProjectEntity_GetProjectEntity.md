---
title: GET Project/{id}
uid: v1ProjectEntity_GetProjectEntity
generated: true
---

# GET Project/{id}

```http
GET /api/v1/Project/{id}
```

Gets a ProjectEntity object.


Calls the Project agent service GetProjectEntity.





| Path Part | Type | Description |
|-----------|------|-------------|
| id | int32 | The id of the ProjectEntity to return. **Required** |


## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category" Default = show all fields. |
| fk | bool |  Load foreign keys on this entity into the ExtraFields property as 'app.device.keyname'='123' pairs. |

```http
GET /api/v1/Project/{id}?$select=name,department,category/id
GET /api/v1/Project/{id}?fk=True
```


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


## Response:

ProjectEntity found.

| Response | Description |
|----------------|-------------|
| 200 | ProjectEntity found. |
| 304 | ProjectEntity has not changed since the requested If-Modified-Since date. |
| 404 | Not Found. |

### Response body: ProjectEntityWithLinks

| Property Name | Type |  Description |
|----------------|------|--------------|
| ProjectId | int32 | Primary key |
| Name | string | Project name |
| ProjectNumber | string | Automatically generated number |
| ProjectMembers | array | The persons which are members of the project |
| Urls | array | The project's internet adresses |
| CreatedDate | date-time | Registered date  in UTC. |
| UpdatedDate | date-time | Last updated date  in UTC. |
| Description | string | The actual text, max 2047 significant characters even though it is stored as a larger data type on some databases |
| Postit | string | The actual text, max 2047 significant characters even though it is stored as a larger data type on some databases |
| CreatedBy | Associate | The person that created the project |
| UpdatedBy | Associate | The person that last updated the project |
| Associate | Associate | The person that created the project  <para>Use MDO List name "associate" to get list items.</para> |
| ProjectStatus | ProjectStatus | Project status is a list defined by the database administrator. Different statuses of a project may be: “In planning”, “Started”, “Finished” and so on  <para>Use MDO List name "projectstatus" to get list items.</para> |
| ProjectType | ProjectType | Project type is a list defined by the database admin. for example: 'Large', 'Small', 'Party'...  <para>Use MDO List name "projecttype" to get list items.</para> |
| HasImage | bool | True if the project has an image. (This is the image that is displayed in the CRM client) |
| ImageDescription | string | Description of the project image if it exists. (This is the image that is displayed in the CRM client) |
| ActiveStatusMonitorId | int32 | Active status monitor identity with the lowest rank for project |
| Links | array | List of all elements linked to the project |
| ActiveLinks | int32 | Number of active links to documents, other appointments, and such |
| Completed | bool | Done (0=false, 1=true). Status implies changes in which fields are shown in GUI, as well as which fields can be updated |
| NextMilestoneDate | date-time | Calculated date, reflects date of closest non-complete future milestone activity |
| NmdAppointmentId | int32 | ID of appointment that "caused" the nextMilestoneDate, can be 0 |
| EndDate | date-time | Planned end date for project, inhertied from type and later editable |
| ActiveErpLinks | int32 | The number of active erp links |
| UserDefinedFields | object | Deprecated: Use {SuperOffice.CRM.Services.ProjectEntity.CustomFields} instead. Dictionary of user defined field data. The key string is the ProgId of the UdefField, or if the ProgId is empty it is a string of the format "SuperOffice:[UdefFieldIdentity]", e.g. "SuperOffice:1234" |
| ExtraFields | object | Deprecated: Use {SuperOffice.CRM.Services.ProjectEntity.CustomFields} instead. Extra fields added to the carrier. This could be data from Plug-ins, the foreign key system, external applications, etc. |
| CustomFields | object | Udef + Extra fields added to the carrier. Extra fields as defined by changes to database schema + user-defined fields as defined by admin. Custom fields combines user defined fields and extra fields into one bucket.  The individual {SuperOffice.CRM.Services.ProjectEntity.ExtraFields} and <see cref="P:SuperOffice.CRM.Services.ProjectEntity.UserDefinedFields">UserDefinedFields</see> properties are deprecated in favor of this combined collection. |
| PublishEventDate | date-time | Publish event date |
| PublishTo | date-time | Publication valid to (inclusive) |
| PublishFrom | date-time | Publication valid from (inclusive) |
| IsPublished | bool | Publication is published |
| TableRight | TableRight | The carrier's table right |
| FieldProperties | object | Field property dictionary mapping field names to field access rights. |
| _Links | object |  |

## Sample request

```http!
GET /api/v1/Project/{id}
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
```

## Sample response

```http_
HTTP/1.1 200 ProjectEntity found.
Content-Type: application/json; charset=utf-8
Last-Modified: Fri, 27 Apr 2007 13:57:19 G4T

{
  "ProjectId": 986,
  "Name": "Crooks Group",
  "ProjectNumber": "1426112",
  "ProjectMembers": [
    {
      "ProjectmemberId": 149,
      "ContactId": 709,
      "ProjectId": 540,
      "ContactName": "Daniel-Okuneva",
      "ContactDepartment": "",
      "ProjectName": "Cruickshank-Littel",
      "EmailId": 60,
      "EmailAddress": "bonnie_cormier@armstrong.biz",
      "CountryId": 494,
      "Firstname": "Delmer",
      "MiddleName": "Reilly, Schneider and Rutherford",
      "Lastname": "Sipes",
      "PersonId": 457,
      "Mrmrs": "laborum",
      "ProjectMemberTypeName": "Howell, Abernathy and Hettinger",
      "Phone": "884-338-5256 x6455",
      "PhoneId": 692,
      "ProjectMemberTypeId": 472,
      "EmailAddressName": "elian_konopelski@howe.co.uk",
      "Comment": "laborum",
      "FullName": "Laurence Miller",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 70
        }
      }
    }
  ],
  "Urls": [
    {
      "Value": "aliquam",
      "StrippedValue": "ut",
      "Description": "Organic zero defect interface",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 310
        }
      }
    },
    {
      "Value": "aliquam",
      "StrippedValue": "ut",
      "Description": "Organic zero defect interface",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 310
        }
      }
    }
  ],
  "CreatedDate": "1996-09-19T13:57:19.0935194+02:00",
  "UpdatedDate": "2007-04-27T13:57:19.0935194+02:00",
  "Description": "Robust discrete infrastructure",
  "Postit": "quia",
  "CreatedBy": null,
  "UpdatedBy": null,
  "Associate": null,
  "ProjectStatus": null,
  "ProjectType": null,
  "HasImage": false,
  "ImageDescription": "Proactive solution-oriented intranet",
  "ActiveStatusMonitorId": 541,
  "Links": [
    {
      "EntityName": "Stoltenberg-Muller",
      "Id": 804,
      "Description": "Virtual mission-critical hierarchy",
      "ExtraInfo": "et",
      "LinkId": 775,
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 538
        }
      }
    }
  ],
  "ActiveLinks": 441,
  "Completed": false,
  "NextMilestoneDate": "2010-12-26T13:57:19.0935194+01:00",
  "NmdAppointmentId": 843,
  "EndDate": "2020-10-06T13:57:19.0935194+02:00",
  "ActiveErpLinks": 789,
  "UserDefinedFields": {
    "SuperOffice:1": "Velma Bradtke",
    "SuperOffice:2": "1042919240"
  },
  "ExtraFields": {
    "ExtraFields1": "ipsam",
    "ExtraFields2": "ea"
  },
  "CustomFields": {
    "CustomFields1": "vitae",
    "CustomFields2": "et"
  },
  "PublishEventDate": "2015-11-08T13:57:19.0935194+01:00",
  "PublishTo": "2007-02-07T13:57:19.0935194+01:00",
  "PublishFrom": "2020-11-09T13:57:19.0935194+01:00",
  "IsPublished": true,
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 89
    }
  },
  "_Links": {
    "Self": "https://www.example.com/api/v1/contact/321",
    "Archive": "https://www.example.com/api/v1/contact"
  }
}
```
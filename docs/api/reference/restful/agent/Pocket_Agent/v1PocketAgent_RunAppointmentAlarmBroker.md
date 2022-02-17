---
title: POST Agents/Pocket/RunAppointmentAlarmBroker
id: v1PocketAgent_RunAppointmentAlarmBroker
---

# POST Agents/Pocket/RunAppointmentAlarmBroker

```http
POST /api/v1/Agents/Pocket/RunAppointmentAlarmBroker
```

Execute the AppointmentAlarmBroker once







## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category". Default = show all fields. |

```http
POST /api/v1/Agents/Pocket/RunAppointmentAlarmBroker?$select=name,department,category/id
```


## Request Headers

| Parameter Name | Description |
|----------------|-------------|
| Authorization  | Supports 'Basic', 'SoTicket' and 'Bearer' schemes, depending on installation type. |
| X-XSRF-TOKEN   | If not using Authorization header, you must provide XSRF value from cookie or hidden input field |
| SO-AppToken | The application token that identifies the partner app. Used when calling Online WebAPI from a server. |


## Response


| Response | Description |
|----------------|-------------|
| 204 | No Content |
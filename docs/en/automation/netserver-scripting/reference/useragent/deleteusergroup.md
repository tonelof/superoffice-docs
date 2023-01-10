---
uid: useragent-deleteusergroup
title: UserAgent.DeleteUserGroup event method
description: Scripting events called on the DeleteUserGroup method on the UserAgent service agent.
so.generated: true
keywords:
  - "netserver"
  - "scripting"
so.date: 11.29.2022
so.topic: reference
so.envir:
  - "onsite"
---
# UserAgent.DeleteUserGroup

Scripting events called on the <see cref='M:SuperOffice.CRM.Services.IUserAgent.DeleteUserGroup'>DeleteUserGroup</see> method on the <see cref='IUserAgent'>IUserAgent</see>  service agent.

## BeforeDeleteUserGroup
```cs
    static void BeforeDeleteUserGroup(
       Int32  userGroupToDelete,
       Int32  userGroupToMoveTo,
       ref object  eventState
      );
```
Executes before the service method is invoked.
It can store some state in the *eventState* parameter, that is passed to the **After** and **AfterAsync** methods in this service call.
Event state is not preserved between different service calls. It is set to null at the start of each service call.
## AfterDeleteUserGroup
```cs
    static void AfterDeleteUserGroup(
       Int32  userGroupToDelete,
       Int32  userGroupToMoveTo,
       ref object  eventState
      );
```
Executes after the service method has been invoked. The service waits for this method to complete before returning the result to the caller.
This service call has no return value, so there is no **returnValue** parameter
Any state you set in the **Before** method is passed in through the *eventState* parameter.
## AfterDeleteUserGroupAsync
```cs
    static void AfterDeleteUserGroupAsync(
       Int32  userGroupToDelete,
       Int32  userGroupToMoveTo,
       ref object  eventState
      );
```
Executes after the service method is invoked, without waiting for the call to return.
The service call is not blocked waiting for this method to complete.
Any state you set in the **Before** method is passed in through the *eventState* parameter.

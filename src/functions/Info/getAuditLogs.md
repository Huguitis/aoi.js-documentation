---
title: $getAuditLogs 
description: $getAuditLogs will retrieve guild audit logs according to the given arguments.
id: getAuditLogs
---

`$getAuditLogs` will retrieve guild audit logs according to the given arguments.

## Usage

```php
$getAuditLogs[limit?;userID?;action?;guildID?;format?]
```

## Parameters 


| Field    | Type    | Description                                                                                                                                                              | Required |
| -------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |:--------:|
| limit?   | integer | the maximum of audit logs it will return                                                                                                                                 |    false    |
| userID?  | integer | the user who executed the action stated in audit logs                                                                                                                    |    false    |
| action?  | integer | the action that was executed  <br /> 1. **all** (default) will retrieve all actions without filtering <br /> 2. You can find all permissions [here][discord-permissions] |    false    |
| guildID? | integer | guild ID                                                                                                                                                                 |    false    |
| format?  | integer | the format to return the audit logs in                                                                                                                                   |    false    |


| Format              |                                                                   |
| ------------------- | ----------------------------------------------------------------- |
| {executor.username} | Will return the username of the user who excuted the action       |
| {executor.mention}  | Will mention the user who executed the action                     |
| {executor.id}       | Will return the user ID of the user who executed the action       |
| {executor.tag}      | Will return the discriminator of the user who executed the action |
| {target.id}         | Will return the ID of the user who was the target of the action   |
| {action}            | Will return the action itself                                     |
| {id}                | Will return the action/auditlog ID                                |


## Example

This will return your latest actions (which are logged in audit logs):

```javascript
bot.command({
  name: 'getAuditLogs',
  code: `
  $getAuditLogs[5;$authorID;All;$guildID;{executor.username}: {target.id} - {action}]
  `
});
```

[discord-permissions]: https://discord.com/developers/docs/topics/permissions
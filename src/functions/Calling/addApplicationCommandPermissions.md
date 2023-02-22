---
title: $addApplicationCommandPermissions 
description: $addApplicationCommandPermissions will change permissions of a slash command.
id: addApplicationCommandPermissions
---

## Usage

```php
$addApplicationCommandPermissions[guildID/global?;id;...perms]
```

## Parameters 


| Field          | Type    | Description            | Required |
| -------------- | ------- | ---------------------- |:--------:|
| guildID/global | string  | global or guildID      |    true   |
| id             | integer | application command ID |    true   |
| ...perms       | string  | permissions            |    true   |


## Example

This will disable the slash command for everyone in the guild ( make sure to replace "ID" with the actual slash command ID ):

```javascript
bot.command({
  name: 'addApplicationCommandPermissions',
  code: `
    $addApplicationCommandPermissions[$guildID;ID;[
  {
    id: '$guildID',
    type: 'ROLE',
    permission: false
  }
]]`
});
```
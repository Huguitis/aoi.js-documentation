---
title: $takeRoles
description: $takeRoles will remove one or multiple roles from a given member.
id: takeRoles
---

`$takeRoles` will remove one or multiple roles from a given member.

## Usage

```php
$takeRoles[guildID;userID;...roleIDs]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| guildID  | integer | guild ID        |   true   |
| userID  | integer | user ID        |   true   |
| ...roleIDs  | integer | role IDs        |   true   |

## Example

This will remove given roles from yourself (the roles must be below the bot's highest role):

```javascript
bot.command({
    name: 'takeRoles',
    code: `
   $takeRoles[$guildID;$authorID;roleID;roleID;...]`
});
```
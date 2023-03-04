---
title: $takeRole
description: $takeRole will remove a given role from a given member.
id: takeRole
---

`$takeRole` will remove a given role from a given member.

## Usage

```php
$takeRole[guildID;userID;roleID]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| guildID  | integer | guild ID        |   true   |
| userID  | integer | user ID        |   true   |
| roleID  | integer | role ID        |   true   |

## Example

This will remove a given role from yourself (the role must be below the bot's highest role):

```javascript
bot.command({
    name: 'takeRole',
    code: `
   $takeRole[$guildID;$authorID;roleID]`
});
```
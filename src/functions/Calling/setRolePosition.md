---
title: $setRolePosition
description: $setRolePosition will set a roles' position.
id: setRolePosition
---

`$setRolePosition` will set a roles' position.

## Usage

```php
$setRolePosition[roleID;position;guildID?]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| roleID  | integer | role ID        |   true   |
| position  | number | new role position (1 being the very bottom)        |   true   |
| guildID?  | integer | guild ID        |   false   |

## Example

This will change a random role's position to `1` (the bot's highest role must be above that role):

```javascript
bot.command({
    name: 'setRolePosition',
    code: `
   $setRolePosition[$randomRoleID;1;$guildID]`
});
```
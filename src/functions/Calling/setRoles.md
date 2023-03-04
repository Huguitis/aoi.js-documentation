---
title: $setRoles
description: $setRoles will set a member's roles.
id: setRoles
---

`$setRoles` will set a member's roles.

## Usage

```php
$setRoles[guildID;memberID;...roleIDs]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| guildID  | integer | guild ID        |   true   |
| memberID  | integer | member ID        |   true   |
| ...roleIDs  | integer | role IDs        |   true   |

## Example

This will either remove or add specific roles from you:

```javascript
bot.command({
    name: 'setRoles',
    code: `
   $setRoles[$guildID;$authorID;roleID1;roleID2;roleID3;....]`
});
```
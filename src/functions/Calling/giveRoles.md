---
title: $giveRoles 
description: $giveRoles will give an specific user multiple or one specific role(s).
id: giveRoles
---

`$giveRoles` will give an specific user multiple or one specific role(s).

## Usage

```php
$giveRoles[guildID;userID;...roles]
```

## Parameters 


| Field   | Type    | Description                                         | Required |
| ------- | ------- | --------------------------------------------------- |:--------:|
| guildID | integer | guild ID                                            |    true   |
| userID  | integer | user ID                                             |    true   |
| roles   | integer | role IDs split by semicolons (roleid;roleid;roleid) |    true   |

Please note that the bots **highest** role must be above the role you're trying to assign.

## Example

This will assign you two role called "Admin" and "Moderator" (if present):

```javascript
bot.command({
  name: 'giveRoles',
  code: `
  $giveRoles[$guildID;$authorID;$findRole[Admin];$findRole[Moderator]]
  `
});
```
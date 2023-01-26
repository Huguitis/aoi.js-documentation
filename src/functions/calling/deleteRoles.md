---
title: $deleteRoles 
description: $deleteRoles will delete one or multiple roles.
id: deleteRoles
---

`$deleteRoles` will delete one or multiple roles.

## Usage

```php
$deleteRoles[guildID;...roles]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| guildID    | integer  | guild ID                             | yes      |
| roles     | string  | id of the roles       | yes       |


## Example

This will delete roles of your guilds ( make sure to add actual IDs )

```javascript
bot.command({
  name: 'deleteRoles',
  code: `
  Deleted three roles!
  $deleteRoles[$guildID;roleID1;roleID2;roleID3]
  `
});
```
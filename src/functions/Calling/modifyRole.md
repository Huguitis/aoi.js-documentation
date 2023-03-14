---
title: $modifyRole
description: $modifyRole will modify a given role.
id: modifyRole
---

`$modifyRole` will modify a given role.

## Usage

```php
$modifyRole[guildID;roleID;...data]
```

## Parameters 

| Field     | Type    | Description                               | Required |
|-----------|---------|-------------------------------------------|:--------:|
| guildID   | integer | guild ID                                  |   true   |
| roleID    | integer | role ID                                   |   true   |
| ...data   |  string | new role data                             |   true   |

## Example

This will edit a existing role / change its name to "Awesome!":

```javascript
bot.command({
    name: 'modifyRole',
    code: `
  $modifyRole[$guildID;roleID;{
    "name": "Awesome!"
  }]
  `
});
```
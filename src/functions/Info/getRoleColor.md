---
title: $getRoleColor 
description: $getRoleColor will return the given role's color.
id: getRoleColor
---

`$getRoleColor` will return the given role's color.

## Usage

```php
$getRoleColor[roleId;guildId?]
```

## Parameters 


| Field    | Type    | Description                                   | Required |
| -------- | ------- | --------------------------------------------- |:--------:|
| roleId   | integer | the role Id of the role you want the color of |    true   |
| guildId? | integer | the guild Id of where the role was created in |    false    |


## Example

This will return the role ID of your highest role:

```javascript
bot.command({
  name: 'getRoleColor',
  code: `
  $getRoleColor[$highestRole]
  `
});
```
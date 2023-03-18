---
title: $setRoleColor
description: $setRoleColor will set a roles' color.
id: setRoleColor
---

`$setRoleColor` will set a roles' color.

## Usage

```php
$setRoleColor[roleID;color]
```

## Parameters

| Field  | Type    | Description | Required |
|--------|---------|-------------|:--------:|
| roleID | integer | role ID     |   true   |
| color  | string  | color       |   true   |

## Examples

This will change a random role's color to red:

```javascript
bot.command({
    name: 'setRoleColor',
    code: `
   $setRoleColor[$randomRoleID;Red]`
});
```

```javascript
bot.command({
    name: 'setRoleColor',
    code: `
   $setRoleColor[$randomRoleID;ED4245]`
});
```
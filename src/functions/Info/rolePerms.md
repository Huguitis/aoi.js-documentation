---
title: $rolePerms
description: $rolePerms will return all given permissions of a role.
id: rolePerms
---

`$rolePerms` will return all given permissions of a role.

## Usage

```php
$rolePerms[roleID;sep?;guildID?]
```

## Parameters

| Field    | Type    | Description                              | Required |
|----------|---------|------------------------------------------|:--------:|
| roleID   | integer | role ID                                  |   true   |
| sep?     | integer | separator to separate multiple arguments |  false   |
| guildID? | integer | guild ID                                 |  false   |

## Example

This will return the permissions for the `@everyone` role:

```javascript
bot.command({
    name: 'rolePerms',
    code: `
  $rolePerms[$guildID;, ;$guildID]
  `
});
```

---
title: $modifyRolePerms
description: $modifyRolePerms will modify a given role's permissions.
id: modifyRolePerms
---

`$modifyRolePerms` will modify a given role's permissions.

## Usage

```php
$modifyRolePerms[guildID;roleID;...perms]
```

## Parameters

| Field    | Type    | Description                                          | Required |
|----------|---------|------------------------------------------------------|:--------:|
| guildID  | integer | guild ID                                             |   true   |
| roleID   | integer | role ID / `$guildID` represents the `@everyone` role |   true   |
| ...perms | string  | permissions                                          |   true   |

|     | Description                                          |
|-----|------------------------------------------------------|
| `-` | Deny a specific permission to someone or something.  |
| `+` | Allow a specific permission to someone or something. |
| `/` | Reset a specific permission to its default state.    |

You can find all permissions __[here](../../guides/9permissionsintents.md)__.

## Example

This will edit a existing role's permission and allow the "@everyone" role to send messages and add reactions.

```javascript
bot.command({
    name: 'modifyRolePerms',
    code: `
  $modifyRolePerms[$guildID;$guildID;+sendmessages;+addreactions]"
  }]
  `
});
```
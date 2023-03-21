---
title: $modifyChannelPerms
description: $modifyChannelPerms will modify a given channels permission overrides.
id: modifyChannelPerms
---

`$modifyChannelPerms` will modify a given channel's permission overrides.

## Usage

```php
$modifyChannelPerms[channelID?;roruId;...perms]
```

## Parameters

| Field     | Type    | Description                                                  | Required |
|-----------|---------|--------------------------------------------------------------|:--------:|
| channelID | integer | channel ID                                                   |   false  |
| roruId    | integer | role or user ID / `$guildID` represents the `@everyone` role |   true   |
| ...perms  | string  | permissions                                                  |   true   |

|     | Description                                          |
|-----|------------------------------------------------------|
| `-` | Deny a specific permission to someone or something.  |
| `+` | Allow a specific permission to someone or something. |
| `/` | Reset a specific permission to its default state.    |

You can find all permissions __[here](../../guides/9permissionsintents.md)__.

## Example

This will allow `@everyone` to send messages and add reactions in the current channel:

```javascript
bot.command({
    name: 'modifyChannelPerms',
    code: `
  $modifyChannelPerms[$channelID;$guildID;+sendmessages;+addreactions]
  `
});
```

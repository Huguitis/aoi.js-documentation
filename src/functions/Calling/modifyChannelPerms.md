---
title: $modifyChannelPerms
description: $modifyChannelPerms will modify a given channels permission overrides.
id: modifyChannelPerms
---

`$modifyChannelPerms` will modify a given channel's permission overrides.

## Usage

```php
$modifyChannelPerms[roruId;channelID;...perms]
```

## Parameters 


| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| roruId    | integer | role or user ID |   true   |
| channelID | integer | channel ID      |   true   |
| ...perms  | string  | permissions     |   true   |

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
  $modifyChannelPerms[$guildID;$channelID;+sendmessages;+addreactions]
  `
  // $guildID represents the @everyone role.
});
```
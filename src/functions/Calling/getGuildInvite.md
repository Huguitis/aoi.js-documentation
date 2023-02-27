---
title: $getGuildInvite
description: $getGuildInvite will create a guild invite.
id: getGuildInvite
---

`$getGuildInvite` will create a guild invite.

## Usage

```php
$getGuildInvite[guildID?;...options]
```

## Parameters

| Field    | Type    | Description  | Required |
|----------|---------|--------------|:--------:|
| guildID? | integer | guild ID     |  false   |
| options? | string  | json objects |  false   |

<details>
  <summary><h3> Invite Target Types </h3></summary>

| TYPE                 | VALUE |
|----------------------|-------|
| STREAM               | 1     |
| EMBEDDED_APPLICATION | 2     |

</details>

## Examples

This will create an invite of the channel where the command is executed in:

```javascript
bot.command({
    name: 'getGuildInvite',
    code: `
  $getGuildInvite[$guildID]
  `
});
```

### Advanced Examples

Create Temporary Invites with limited uses:

```javascript
bot.command({
    name: 'getGuildInvite',
    code: `
  $getGuildInvite[$guildID;{
            "temporary": true,
            "maxAge": 650,
            "maxUses": 25,
            "unique": true
  }]
  `
});
```

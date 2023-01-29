---
title: $createServerInvite 
description: $createServerInvite will create a guild invite.
id: createServerInvite
---

`$createServerInvite` will create a guild invite.

## Usage

```php
$createServerInvite[guildID?;...options]
```

## Parameters 


| Field    | Type    | Description  | Required |
| -------- | ------- | ------------ |:--------:|
| guildID? | integer | guild ID     |    no    |
| options? | string  | json objects |    no    |

<details>
  <summary><h3> Invite Target Types </h3></summary>

| TYPE                 | VALUE |
| -------------------- | ----- |
| STREAM               | 1     |
| EMBEDDED_APPLICATION | 2     |

</details>

## Examples

This will create an invite of the channel where the command is executed in:

```javascript
bot.command({
  name: 'createServerInvite',
  code: `
  $createServerInvite[$guildID]
  `
});
```

### Advanced Examples

Create Temporary Invites with limited uses:

```javascript
bot.command({
  name: 'createServerInvite',
  code: `
  $createServerInvite[$guildID;{
            "temporary": true,
            "maxAge": 650,
            "maxUses": 25,
            "unique": true
  }]
  `
});
```

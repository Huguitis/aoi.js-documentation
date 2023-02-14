---
title: $guildMFALevel 
description: $guildMFALevel will return the guild's MFA Level.
id: guildMFALevel
---

`$guildMFALevel` will return the guild's MFA Level.

## Usage

```php
$guildMFALevel[guildID?]
```

## Parameters 


| Field    | Type    | Description | Required |
| -------- | ------- | ----------- |:--------:|
| guildID? | integer | guild ID    |    false    |

| Type |                                                         |
| ---- | ------------------------------------------------------- |
| 0    | guild has false MFA/2FA requirement for moderation actions |
| 1    | guild has a 2FA requirement for moderation actions      |

## Example

This will return the guild's MFA Level:

```javascript
bot.command({
  name: 'guildMFALevel',
  code: `
  $guildMFALevel[$guildID]
  `
});
```

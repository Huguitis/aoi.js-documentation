---
title: $ban
description: $ban will ban a user of a given guild.
id: ban
---

`$ban` will ban a user of a guild.

## Usage

```php
$ban[guildID?;userID;days?;reason?]
```

## Parameters

| Field    | Type    | Description                                                      | Required |
|----------|---------|------------------------------------------------------------------|:--------:|
| guildID? | integer | guild ID                                                         |  false   |
| userID   | integer | user ID to ban                                                   |   true   |
| days?    | string  | days of message history to delete, cannot be higher than 14 days |  false   |
| reason?  | string  | ban reason                                                       |  false   |

## Example(s)

This will ban a random user of your guild:

```javascript
bot.command({
    name: 'ban',
    code: `
  $ban[$guildID;$randomUserID;7;Imagine getting banned.]
  `
});
```

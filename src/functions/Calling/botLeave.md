---
title: $botLeave
description: $botLeave will make your bot leave a specific server.
id: botLeave
---

`$botLeave` will make your bot leave a specific server.

## Usage

```php
$botLeave[guildID?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|:--------:|
| guildID? | integer | guild ID    |  false   |

## Example

This will make your bot leave the current guild:

```javascript
bot.command({
    name: 'botLeave',
    code: `
  $botLeave[$guildID]
  $wait[2s]
  $sendMessage[Bye, I'm leaving!]
  `
});
```

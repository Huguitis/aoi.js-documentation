---
title: $emojiCount
description: $emojiCount will return the emoji count of a guild.
id: emojiCount
---

`$emojiCount` will return the emoji count of a guild.

## Usage

```php
$emojiCount[guildID?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|:--------:|
| guildID? | integer | guild ID    |  false   |

## Example

This will return the emoji count of your guild:

```javascript
bot.command({
    name: 'emojiCount',
    code: `
  You have $emojiCount emojis in your guild!
  `
});
```
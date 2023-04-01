---
title: $guildEmojiExists
description: $guildEmojiExists will check if the given emoji exists in the given guild.
id: guildEmojiExists
---

`$guildEmojiExists` will check if the given emoji exists in the given guild.

## Usage

```php
$guildEmojiExists[emoji;guildId?]
```

## Parameters

| Field    | Type    | Description                                  | Required |
|----------|---------|----------------------------------------------|----------|
| emoji    | string  | emoji you want to check if it exists         | true     |
| guildId? | integer | guild id of the guild where the emoji exists | false    |

**Please note that your bot has to be present in the guild where the emoji is in, only exception are webhooks.**

## Example(s)

This will return `true` as
the ![emoji](https://cdn.discordapp.com/emojis/1003365344724910191.webp?size=16&quality=lossless) emoji exists:

```javascript
bot.command({
    name: 'guildEmojiExists',
    code: `
  $guildEmojiExists[<:LerefMoney:1003365344724910191>;$guildID]
  `
});
```

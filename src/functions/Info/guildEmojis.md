---
title: $guildEmojis
description: $guildEmojis will return the emojis of a specific guild.
id: guildEmojis
---

`$guildEmojis` will return the emojis of a specific guild.

## Usage

```php
$guildEmojis[sep?;guildID?]
```

## Parameters

| Field    | Type    | Description                                   | Required |
|----------|---------|-----------------------------------------------|:--------:|
| sep?     | string  | the separator to separate the returned emojis |  false   |
| guildID? | integer | guild ID                                      |  false   |

## Example(s)

This will return the emojis of your guild:

```javascript
bot.command({
    name: 'guildEmojis',
    code: `
  $guildEmojis[, ;$guildID]
  `
});
```

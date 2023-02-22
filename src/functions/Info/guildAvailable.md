---
title: $guildAvailable
description: $guildAvailable will return if the given guild is available on Discord.
id: guildAvailable
---

`$guildAvailable` will return if the given guild is available on Discord.

## Usage

```php
$guildAvailable[guildID?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|:--------:|
| guildID? | integer | guild ID    |  false   |

## Example

This will return `true` or `false` depending on if the guild is available:

```javascript
bot.command({
    name: 'guildAvailable',
    code: `
  $guildAvailable[$guildID]
  `
});
```

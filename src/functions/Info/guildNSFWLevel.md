---
title: $guildNSFWLevel
description: $guildNSFWLevel will return the guild's NSFW level.
id: guildNSFWLevel
---

`$guildNSFWLevel` will return the guild's NSFW level.

## Usage

```php
$guildNSFWLevel[guildID?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|:--------:|
| guildID? | integer | guild ID    |   true   |

## Example

This will return the guild's NSFW level:

```javascript
bot.command({
    name: 'guildNSFWLevel',
    code: `
  $guildNSFWLevel[$guildID]
  `
});
```

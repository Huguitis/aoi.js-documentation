---
title: $guildDescription
description: $guildDescription will return the guild's description.
id: guildDescription
---

`$guildDescription` will return the guild's description.

## Usage

```php
$guildDescription[guildID?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|:--------:|
| guildID? | integer | guild ID    |  false   |

## Example

This will return the description of a specific guild:

```javascript
bot.command({
    name: 'guildDescription',
    code: `
  $guildDescription[$guildID]
  `
});
```

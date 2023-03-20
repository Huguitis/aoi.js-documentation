---
title: $guildNames
description: $guildNames will return the guide names your bot is in.
id: guildNames
---

`$guildNames` will return the guide names your bot is in.

## Usage

```php
$guildNames[sep?]
```

## Parameters

| Field | Type   | Description                              | Required |
|-------|--------|------------------------------------------|:--------:|
| sep?  | string | separator to seperate multiple arguments |  false   |

## Example

This will return the names of the guilds your bot is in and seperate it by a comma:

```javascript
bot.command({
    name: 'guildNames',
    code: `
  $guildNames[, ]
  `
});
```

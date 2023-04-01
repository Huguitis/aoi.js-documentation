---
title: $log
description: $log will log a given message in your bot's console.
id: log
---

`$log` will log a given message in your bot's console.

## Usage

```php
$log[message]
```

## Parameters

| Field   | Type   | Description    | Required |
|---------|--------|----------------|:--------:|
| message | string | message to log |   true   |

## Example(s)

This will log "Aoi.js is great!" in your bot's console:

```javascript
bot.command({
    name: "log",
    code: `
    $log[Aoi.js is great!]
    `
});
```
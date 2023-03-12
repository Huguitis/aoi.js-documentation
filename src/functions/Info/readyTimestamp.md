---
title: $readyTimestamp
description: $readyTimestamp will return the timestamp of when the bot was ready.
id: readyTimestamp
---

`$readyTimestamp` will return the timestamp of when the bot was ready.

## Usage

```php
$readyTimestamp
```

## Example

This will return the last time your bot when online:

```javascript
bot.command({
    name: 'readyTimestamp',
    code: `
  $readyTimestamp
  `
});
```

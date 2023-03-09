---
title: $shutdown
description: $shutdown will shutdown / end the process of your bot.
id: shutdown
---

`$shutdown` will shutdown / end the process of your bot.

## Usage

```php
$shutdown
```

## Example

This will shutdown your bot:

```javascript
bot.command({
    name: "shutdown",
    code: `
    $shutdown
    `
});
```
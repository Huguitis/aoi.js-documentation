---
title: $nodeVersion
description: $nodeVersion will return your current nodejs version.
id: nodeVersion
---

`$nodeVersion` will return your current nodejs version.

## Usage

```php
$nodeVersion
```

## Examples

This will return the current nodejs version your bot is running on:

```javascript
bot.command({
    name: "nodeVersion",
    code: `
    $nodeVersion
    `
});
```
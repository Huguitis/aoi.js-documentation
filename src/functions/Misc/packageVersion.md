---
title: $packageVersion
description: $packageVersion will return your current aoi.js version.
id: packageVersion
---

`$packageVersion` will return your current aoi.js version.

## Usage

```php
$packageVersion
```

## Examples

This will return your current aoi.js version:

```javascript
bot.command({
    name: "packageVersion",
    code: `
    $packageVersion
    `
});
```
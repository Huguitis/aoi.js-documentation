---
title: $killClient
description: $killClient will forcefully shutdown your bot.
id: killClient
---

`$killClient` will forcefully shutdown your bot.

## Usage

```php
$killClient
```

## Example

This will forcefully shutdown your bot:

```javascript
bot.command({
    name: "killClient",
    code: `
    $killClient
    `
});
```
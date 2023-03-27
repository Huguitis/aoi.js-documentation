---
title: $clearQueue
description: $clearQueue will clear the current player's queue. 
id: clearQueue
---

`$clearQueue` will clear the current player's queue. 

## Usage

```php
$clearQueue
```

## Example

This will clear the current queue:

```javascript
bot.command({
    name: 'clearQueue',
    code: `
    $clearQueue
  `
});
```
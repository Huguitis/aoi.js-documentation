---
title: $deleteCommand 
description: $deleteCommand will delete the initial command message.
id: deleteCommand
---

`$deleteCommand` will delete the initial command message.

## Usage

```php
$deleteCommand
```

## Example

This will delete the initial command message:

```javascript
bot.command({
  name: 'deleteCommand',
  code: `
  Hello!
  $deleteCommand
  `
});
```

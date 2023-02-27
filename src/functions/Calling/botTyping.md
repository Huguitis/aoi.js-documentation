---
title: $botTyping
description: $botTyping will make your bot type in a channel (show that it's typing).
id: botTyping
---

`$botTyping` will make your bot type in a channel (show that it's typing).

## Usage

```php
$botTyping
```

## Example

This will display your bot as typing and send "Hello!" as message:

```javascript
bot.command({
    name: 'botTyping',
    code: `
  Hello!
  $botTyping
  `
});
```

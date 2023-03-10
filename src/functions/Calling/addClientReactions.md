---
title: $addClientReactions
description: $addClientReactions will add a reaction to the bot's message.
id: addClientReactions
---

`$addClientReactions` will add a reaction to the bot's message.

## Usage

```php
$addClientReactions[...reactions]
```

## Parameters

| Field     | Type   | Description      | Required |
|-----------|--------|------------------|:--------:|
| reactions | string | reactions to add |   true   |

## Example

This will add the given emojis to the bot's response ("Hello!"):

```javascript
bot.command({
    name: 'addClientReactions',
    code: `
    Hello!
    $addClientReactions[🧡;❤]
  `
});
```
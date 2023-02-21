---
title: $addCmdReactions 
description: $addCmdReactions will add a reaction to the bot's message.
id: addCmdReactions
---

`$addCmdReactions` will add a reaction to the bot's message.

## Usage

```php
$addCmdReactions[...reactions]
```

## Parameters 


| Field     | Type   | Description      | Required |
| --------- | ------ | ---------------- |:--------:|
| reactions | string | reactions to add |    true   |

## Example

This will add the given emojis to the bot's response ("Hello!"):

```javascript
bot.command({
  name: 'addCmdReactions',
  code: `
Hello!
$addCmdReactions[🧡;❤]
  `
});
```

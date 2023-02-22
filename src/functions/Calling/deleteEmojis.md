---
title: $deleteEmojis
description: $deleteEmojis will delete multiple emoji.
id: deleteEmojis
---

`$deleteEmojis` will delete multiple emoji.

## Usage

```php
$deleteEmojis[...emojis]
```

## Parameters

| Field  | Type   | Description                 | Required |
|--------|--------|-----------------------------|:--------:|
| emojis | string | emoji name, id or full form |   true   |

## Example

This will delete two random emojis of your guild:

```javascript
bot.command({
    name: 'deleteEmojis',
    code: `
  $deleteEmojis[$randomEmoji;$randomEmoji]
  `
});
```

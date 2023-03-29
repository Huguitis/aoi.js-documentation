---
title: $customEmoji
description: $customEmoji will return a custom emoji.
id: customEmoji
---

`$customEmoji` will return a custom emoji.

## Usage

```php
$customEmoji[emoji;id?]
```

## Parameters

| Field | Type   | Description                                                                                | Required |
|-------|--------|--------------------------------------------------------------------------------------------|:--------:|
| emoji | string | emoji name or id                                                                           |   true   |
| id?   | string | where the emoji is from <br /> 1. **global** <br /> 2. **guildID** - replace with guild ID |  false   |

## Example(s)

This send a custom emoji of your choice, replace emojiname with an actual emoji name:

```javascript
bot.command({
    name: 'customEmoji',
    code: `
  $customEmoji[emojiname]
  `
});
```
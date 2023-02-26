---
title: $modifyEmoji
description: $modifyEmoji will modify a given custom emoji.
id: modifyEmoji
---

`$modifyEmoji` will modify a given custom emoji.

## Usage

```php
$modifyEmoji[guildID;emojiID;name;...roles?]
```

## Parameters 


| Field     | Type    | Description                               | Required |
|-----------|---------|-------------------------------------------|:--------:|
| guildID   | integer | guild ID                                  |   true   |
| emojiID   | integer | emoji ID                                  |   true   |
| name      | string  | new emoji name                            |   true   |
| ...roles? | integer | roles that will be able to use that emoji |  false   |



## Example

This will edit a existing emoji / change its name to "Example":

```javascript
bot.command({
    name: 'modifyEmoji',
    code: `
  $modifyEmoji[$guildID;emojiID;Example]
  `
});
```
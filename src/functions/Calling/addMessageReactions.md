---
title: $addMessageReactions
description: $addMessageReactions will add a reaction to a specific message.
id: addMessageReactions
---

`$addMessageReactions` will add a reaction to a specific message.

## Usage

```php
$addMessageReactions[channelID;messageID;...reactions]
```

## Parameters

| Field     | Type    | Description | Required |
|-----------|---------|-------------|:--------:|
| channelID | integer | channel ID  |   true   |
| messageID | integer | message ID  |   true   |
| reactions | string  | reactions   |   true   |

## Example

This will add the given reactions to your message:

```javascript
bot.command({
    name: 'addMessageReactions',
    code: `
 $addMessageReactions[$channelID;$messageID;✅;❌]
  `
});
```

---
title: $clearReaction
description: $clearReaction will remove a given reaction of a message.
id: clearReaction
---

`$clearReaction` will remove a given reaction of a message.

## Usage

```php
$clearReaction[channelID;messageID;userID;emoji]
```

## Parameters

| Field     | Type    | Description                         | Required |
|-----------|---------|-------------------------------------|:--------:|
| channelID | integer | channel ID                          |   true   |
| messageID | integer | message ID                          |   true   |
| userID    | integer | user ID to remove from the reaction |   true   |
| emoji     | string  | emoji to remove                     |   true   |

## Example(s)

This will add and remove the bot's reaction after two seconds:

```javascript
bot.command({
    name: 'clearReaction',
    code: `
  $clearReaction[$channelID;$messageID;$clientID;🥱]
  $wait[2s]
  $addCmdReactions[🥱]
  `
});
```

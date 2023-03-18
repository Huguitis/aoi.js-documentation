---
title: $userReacted
description: $userReacted will check if a specified user reacted with a specific emoji to a specific message and return
either true or false.
id: userReacted
---

`$userReacted` will check if a specified user reacted with a specific emoji to a specific message and return either true
or false.

## Usage

```php
$userReacted[channelID;messageID;userID;emoji]
```

## Parameters

| Field     | Type    | Description        | Required |
|-----------|---------|--------------------|:--------:|
| guildID   | integer | guild ID           |   true   |
| messageID | integer | message ID         |   true   |
| userID    | integer | user ID            |   true   |
| emoji     | string  | emoji to check for |   true   |

## Example

This will return `true` as your bot reacted to your initial command message:

```javascript
bot.command({
    name: 'userReacted',
    code: `
$userReacted[$channelID;$messageID;$clientID;😩]
$addCmdReactions[😩]
  `
});
```

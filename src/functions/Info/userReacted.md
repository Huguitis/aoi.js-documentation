---
title: $userReacted 
description: $userReacted will check if a specified user reacted with a specific emoji to a specific message and return either true or false.
id: userReacted
---

`$userReacted` will check if a specified user reacted with a specific emoji to a specific message and return either true or false.

## Usage

```php
$userReacted[channelID;messageID;userID;emoji]
```

## Parameters 


| Field     | Type    | Description        | Required |
| --------- | ------- | ------------------ |:--------:|
| guildID   | integer | guild ID           |    yes   |
| messageID | integer | message ID         |    yes   |
| userID    | integer | user ID            |    yes   |
| emoji     | string  | emoji to check for |    yes   |


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

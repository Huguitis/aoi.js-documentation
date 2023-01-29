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
| --------- | ------- | ----------- |:--------:|
| channelID | integer | channel ID  |    yes   |
| messageID | integer | message ID  |    yes   |
| reactions | string  | reactions   |    yes   |


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

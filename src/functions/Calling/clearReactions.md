---
title: $clearReactions
description: $clearReactions will remove a given or all reactions of a message.
id: clearReactions
---

`$clearReactions` will remove a given or all reactions of a message.

## Usage

```php
$clearReactions[channelID;messageID;emoji]
```

## Parameters 


| Field     | Type    | Description                                                                 | Required |
| --------- | ------- | --------------------------------------------------------------------------- |:--------:|
| channelID | integer | channel ID                                                                  |    yes   |
| messageID | integer | message ID                                                                  |    yes   |
| emoji     | string  | emoji to remove <br /> 1. **all** (default) <br /> 2. **emoji** - any emoji |    yes   |


## Example

This will add two emojis and remove one completely:

```javascript
bot.command({
  name: 'clearReactions',
  code: `
  $clearReactions[$channelID;$messageID;🥱]
  $wait[2s]
  $addCmdReactions[🥱;😩]
  `
});
```

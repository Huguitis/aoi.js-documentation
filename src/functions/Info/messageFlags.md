---
title: $messageFlags 
description: $messageFlags will return a message's flags.
id: messageFlags
---

`$messageFlags` will return a message's flags.

## Usage

```php
$messageFlags[messageID;sep?;channelID?]
```

## Parameters 


| Field      | Type    | Description                                   | Required |
| ---------- | ------- | --------------------------------------------- |:--------:|
| messageID  | integer | message id to return flags of                 |    true   |
| sep?       | string  | seperator to seperate returned arguments      |    false    |
| channelID? | integer | channel id of where the message is located in |    false    |


## Example

This will the message flags of your initial command message:

```javascript
bot.command({
  name: 'messageFlags',
  code: `
  $messageFlags[$messageID;, ;$channelID]
  `
});
```

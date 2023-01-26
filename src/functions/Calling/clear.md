---
title: $clear
description: $clear will delete the amount of given messages in a channel.
id: clear
---

`$clear` will delete the amount of given messages in a channel.

## Usage

```php
$clear[amount;filter?;returnCount?;channelID?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| amount    | integer  | amount of messages to clear  | yes      |
| filter?    | string  | filter the messages which are to delete <br /> 1. **everyone** (default) <br /> 2. **unPins** <br /> 3. **bot** <br /> 4.**userID**   | no      |
| returnCount?    | string  | return the count of deleted messages <br /> 1. **no** (default) <br /> 2. **yes**                             | no      |
| channelID?    | integer  | channel ID                             | no      |


## Example

This will delete the most recent fifty messages which are not pinned:

```javascript
bot.command({
  name: 'clear',
  code: `
  $clear[50;unPins;no;$channelID]
  `
});
```

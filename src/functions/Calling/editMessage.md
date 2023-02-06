---
title: $editMessage 
description: $editMessage will edit a given message.
id: editMessage
---

`$editMessage` will edit a given message.

## Usage

```php
$editMessage[messageID;msg;channelID?]
```

## Parameters 


| Field      | Type    | Description | Required |
| ---------- | ------- | ----------- |:--------:|
| messageID  | integer | message ID  |    yes   |
| msg        | string  | new message |    yes   |
| channelID? | integer | channel ID  |    no    |


## Example

This will edit the sent message after five seconds: (alternative to `$editIn`)

```javascript
bot.command({
  name: 'editMessage',
  code: `
  $editMessage[$get[id];Bye!]
  $wait[5s]
  $let[id;$sendMessage[Hello!;true]]
  `
});
```
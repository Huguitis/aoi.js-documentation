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
| messageID  | integer | message ID  |    true   |
| msg        | string  | new message |    true   |
| channelID? | integer | channel ID  |    false    |


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
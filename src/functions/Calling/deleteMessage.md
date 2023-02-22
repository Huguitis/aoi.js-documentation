---
title: $deleteMessage
description: $deleteMessage will delete a specific message.
id: deleteMessage
---

`$deleteMessage` will delete a specific message.

## Usage

```php
$deleteMessage[messageID;channelID]
```

## Parameters

| Field     | Type    | Description | Required |
|-----------|---------|-------------|:--------:|
| messageID | integer | guild ID    |   true   |
| channelID | integer | channel ID  |  false   |

## Example

This will send and delete the sent message after 15 seconds ( we are using $let and $get to temporary store the message
ID ):

```javascript
bot.command({
    name: 'deleteMessage',
    code: `
  $deleteMessage[$get[id];$channelID]
  $let[id;$sendMessage[Hello!;true]]
  `
});
```
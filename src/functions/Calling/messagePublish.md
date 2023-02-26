---
title: $messagePublish
description: $messagePublish will publish a message in an announcement channel.
id: messagePublish
---

`$messagePublish` will publish a message in an announcement channel.

## Usage

```php
$messagePublish[messageID;channelID?]
```

## Parameters 


| Field      | Type    | Description | Required |
|------------|---------|-------------|:--------:|
| messageID  | integer | message ID  |   true   |
| channelID? | integer | channel ID  |   false  |

## Example

This will publish a message ( will only work in announcement channels ):

```javascript
bot.command({
    name: 'messagePublish',
    code: `
  $messagePublish[$get[msgID];$channelID]
  $let[msgID;$sendMessage[Hello!;true]]
  `
});
```
---
title: $channelSendMessage
description: $channelSendMessage will send a message in a specific channel.
id: channelSendMessage
---

`$channelSendMessage` will send a message in a specific channel.

## Usage

```php
$channelSendMessage[channelID;message;returnID?]
```

## Parameters

| Field     | Type    | Description                                                            | Required |
|-----------|---------|------------------------------------------------------------------------|:--------:|
| channelID | integer | channel ID                                                             |   true   |
| message   | string  | message to send                                                        |   true   |
| returnID? | string  | return the message ID <br /> 1. **true** <br /> 2. **false** (default) |  false   |

## Example(s)

This will send "Hello":

```javascript
bot.command({
    name: 'channelSendMessage',
    code: `
  $channelSendMessage[$channelID;Hello]
  `
});
```

### Embeds

This will send an embed with description and footer:

```javascript
bot.command({
    name: 'channelSendMessage',
    code: `
  $channelSendMessage[$channelID;{newEmbed:{title:Hello}{footer:Bye}};false]
  `
});
```

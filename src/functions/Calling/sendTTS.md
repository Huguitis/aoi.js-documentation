---
title: $sendTTS
description: $sendTTS will send a text-to-speech message in a given channel.
id: sendTTS
---

`$sendTTS` will send a text-to-speech message in a given channel.

## Usage

```php
$sendTTS[channelID;message;returnID?]
```

## Parameters

| Field     | Type    | Description                                                         | Required |
|-----------|---------|---------------------------------------------------------------------|:--------:|
| channelID | integer | channel ID                                                          |   true   |
| message   | string  | message to send                                                     |   true   |
| returnID? | string  | return message ID  <br /> 1. **true** <br /> 2. **false** (default) |  false   |

## Example(s)

This will send a TTS message in the current channel:

```javascript
bot.command({
    name: 'sendTTS',
    code: `
   $sendTTS[$channelIDHello!;false]
  `
});
```
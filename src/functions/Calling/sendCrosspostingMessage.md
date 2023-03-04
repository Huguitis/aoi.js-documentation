---
title: $sendCrosspostingMessage
description: $sendCrosspostingMessage will crosspost a given message to the given channels.
id: sendCrosspostingMessage
---

`$sendCrosspostingMessage` will crosspost a given message to the given channels.

## Usage

```php
$sendCrosspostingMessage[message;...channelIDs]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| message  | string | message to send        |   true   |
| ...channelIDs  | integer | channel IDs       |   true   |

## Example

This will crosspost a message to multiple channels in your server:

```javascript
bot.command({
    name: 'sendCrosspostingMessage',
    code: `
   $sendCrosspostingMessage[Hello!;$channelID;$randomChannelID]
  `
});
```
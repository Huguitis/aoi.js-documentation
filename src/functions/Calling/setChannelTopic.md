---
title: $setChannelTopic
description: $setChannelTopic will modify a channel's topic.
id: setChannelTopic
---

`$setChannelTopic` will modify a channel's topic.

## Usage

```php
$setChannelTopic[channelID;topic]
```

## Parameters 

| Field     | Type    | Description | Required |
|-----------|---------|-------------|:--------:|
| channelID | integer | channel ID  |   true   |
| topic     | string  | new topic   |   true   |

## Example

This will change the topic of the channel where the command is exected in:

```javascript
bot.command({
    name: 'setChannelTopic',
    code: `
   $setChannelTopic[$channelID;Hello! This is the new channel topic!]`
});
```
---
title: $getReaction
description: $getReaction will return properties about a given reaction on a specific message.
id: getReaction
---

`$getReaction` will return properties about a given reaction on a specific message.

## Usage

```php
$getReaction[channelID;messageID;reaction;force?;option?]
```

## Parameters

| Field     | Type    | Description                                                                                                                                                    | Required |
|-----------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------:|
| channelID | integer | channel ID of where the message is located in                                                                                                                  |   true   |
| messageID | integer | message ID of the message                                                                                                                                      |   true   |
| reaction  | string  | the reaction its information will be returned of                                                                                                               |   true   |
| force?    | string  | force the action <br /> 1. **true** (default) <br /> 2. **false**                                                                                              |  false   |
| option?   | string  | how it will return the users who reacted to that message <br /> 1. **username** (default) - returns the usernames   <br /> 2. **mention** - mentions the users |  false   |

#### Please note that this won't work without the `GuildMessageReactions` intent.

## Example

This will mention all users that reacted to your message, in this case, only your bot:

```javascript
bot.command({
    name: 'getReaction',
    code: `
$getReaction[$channelID;$messageID;👋;true;mention]
$addClientReactions[👋]
  `
});
```
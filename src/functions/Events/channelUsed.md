---
title: $channelUsed
description: $channelUsed will return the channel ID of where the callback was triggered.
id: channelUsed
---

`$channelUsed` will return the channel ID of where the callback was triggered.

## Usage

```php
$channelUsed
```

## Example(s)

This will return the amount of roles of your guild:

#### You require `onMessageDelete` in your main file in order to use this example!

```javascript
bot.deletedCommand({
    channel: "channelID",
    code: `$userTag deleted a message in <#$channelUsed>!`
});
```

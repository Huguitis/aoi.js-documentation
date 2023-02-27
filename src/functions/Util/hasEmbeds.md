---
title: $hasEmbeds
description: $hasEmbeds will check if there are embeds attached to the message.
id: hasEmbeds
---

`$hasEmbeds` will check if there are embeds attached to the message.

## Usage

```php
$hasEmbeds[messageID;channelID]
```

## Parameters

| Field     | Type    | Description                                             | Required |
|-----------|---------|---------------------------------------------------------|----------|
| messageID | integer | message ID of the embed                                 | true     |
| channelID | integer | channel ID of the channel where the embed is present in | true     |

## Example

This will return `false` as there are false embeds attached to your message:

```javascript
bot.command({
    name: 'hasEmbeds',
    code: `
  $hasEmbeds[$messageID;$channelID]
  `
});
```

---
title: $deleteChannel
description: $deleteChannel will delete a specific channel.
id: deleteChannel
---

`$deleteChannel` will delete a specific channel.

## Usage

```php
$deleteChannel[channelID]
```

## Parameters

| Field     | Type    | Description | Required |
|-----------|---------|-------------|:--------:|
| channelID | integer | channel ID  |   true   |

## Example(s)

This will delete the channel where the command was executed in:

```javascript
bot.command({
    name: 'deleteChannel',
    code: `
  $deleteChannel[$channelID]
  `
});
```

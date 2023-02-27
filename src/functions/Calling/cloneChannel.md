---
title: $cloneChannel
description: $cloneChannel will clone a channel.
id: cloneChannel
---

`$cloneChannel` will clone a channel.

## Usage

```php
$cloneChannel[channelID;name;returnID?]
```

## Parameters

| Field     | Type    | Description                | Required |
|-----------|---------|----------------------------|:--------:|
| channelID | integer | channel ID to clone        |   true   |
| name      | string  | name of the cloned channel |   true   |
| returnID? | string  | return channel ID          |  false   |

### It won't clone any messages of that channel.

## Example

This will clone the current channel and name it "new channel":

```javascript
bot.command({
    name: 'cloneChannel',
    code: `
  $cloneChannel[$channelID;new channel;false]
  `
});
```

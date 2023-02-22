---
title: $guildAFKChannelID
description: $guildAFKChannelID will return a guild's AFK voice channel.
id: guildAFKChannelID
---

`$guildAFKChannelID` will return a guild's AFK voice channel

## Usage

```php
$guildAFKChannelID[guildID?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|:--------:|
| guildID? | integer | guild ID    |   true   |

## Example

This will return the AFK voice channel of your guild:

```javascript
bot.command({
    name: 'guildAFKChannelID',
    code: `
  $guildAFKChannelID
  `
});
```

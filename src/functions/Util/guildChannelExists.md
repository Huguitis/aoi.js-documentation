---
title: $guildChannelExists
description: $guildChannelExists will check if the given guild channel exists.
id: guildChannelExists
---

`$guildChannelExists` will check if the given guild channel exists.

## Usage

```php
$guildChannelExists[channel;guildID?]
```

## Parameters

| Field   | Type    | Description                                       | Required |
|---------|---------|---------------------------------------------------|----------|
| channel | string  | channel ID or name of the guild channel           | true     |
| guildId | integer | id of the guild where the guild channel exists in | true     |

## Example

This will check if a guild channel with the name `rules` exists, alternatively you could use the channel ID instead:

```javascript
bot.command({
    name: 'guildChannelExists',
    code: `
  $guildChannelExists[rules]
  `
});
```

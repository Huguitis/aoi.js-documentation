---
title: $systemChannelID
description: $systemChannelID will return the ID of the guild's system channel.
id: systemChannelID
---

`$systemChannelID` will return the ID of the guild's system channel.

## Usage

```php
$systemChannelID[guildID?]
```

## Parameters

| Field    | Type    | Description   | Required |
| -------- | ------- | ------------- | :------: |
| guildID? | integer | The guild ID. |  false   |

## Example(s)

This will return the guild's system channel ID:

```javascript
bot.command({
    name: 'systemChannelID',
    code: `
  $systemChannelID[$guildID]
  `
});
```

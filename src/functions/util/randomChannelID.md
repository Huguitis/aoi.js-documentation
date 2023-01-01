---
title: $randomChannelID 
description: $randomChannelID will return a random channel ID of all guilds or of a specific guild.
id: randomChannelID
---

`$randomChannelID` will return a random channel ID of all guilds or of a specific guild.

## Usage

```php
$randomChannelID[guildID/global?;type?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| guildID/global?      | string  | guild ID or global search                             | no      |
| type?     | number  |           | no       |


## Example

This will return a random channel ID of your guild:

```javascript
bot.command({
  name: 'randomChannelID',
  code: `
  <#$randomChannelID[$guildID;all]>
  `
});
```

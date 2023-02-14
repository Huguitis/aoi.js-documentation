---
title: $guildPreferredLocale 
description: $guildPreferredLocale will return a guild's set locale.
id: guildPreferredLocale
---

`$guildPreferredLocale` will return a guild's set locale.

## Usage

```php
$guildPreferredLocale[guildID?]
```

## Parameters 


| Field    | Type    | Description | Required |
| -------- | ------- | ----------- |:--------:|
| guildID? | integer | guild ID    |    no    |


## Example

This will return the guild's preferred locale:

```javascript
bot.command({
  name: 'guildPreferredLocale',
  code: `
  $guildPreferredLocale[$guildID]
  `
});
```

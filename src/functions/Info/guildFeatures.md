---
title: $guildFeatures 
description: $guildFeatures will return unlocked guild features.
id: guildFeatures
---

`$guildFeatures` will return unlocked guild features.

## Usage

```php
$guildFeatures[guildID?]
```

## Parameters 


| Field    | Type    | Description | Required |
| -------- | ------- | ----------- |:--------:|
| guildID? | integer | guild ID    |    no    |


## Example

This will return the unlocked guild features of a guild:

```javascript
bot.command({
  name: 'guildFeatures',
  code: `
  $guildFeatures[$guildID;yes]
  `
});
```

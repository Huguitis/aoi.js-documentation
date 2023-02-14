---
title: $guildExists 
description: $guildExists will check if the given guild exists.
id: guildExists
---

`$guildExists` will check if the given guild exists.

## Usage

```php
$guildExists[guildId]
```

## Parameters 


| Field   | Type    | Description | Required |
| ------- | ------- | ----------- | -------- |
| guildId | integer | guild id    | yes      |


## Example

This will return `true` your guild exists:

```javascript
bot.command({
  name: 'guildExists',
  code: `
  $guildExists[$guildID]
  `
});
```
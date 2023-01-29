---
title: $guildVerificationLevel 
description: $guildVerificationLevel will return the guild's verification level.
id: guildVerificationLevel
---

`$guildVerificationLevel` will return the guild's verification level.

## Usage

```php
$guildVerificationLevel[guildID?]
```

## Parameters 


| Field    | Type    | Description | Required |
| -------- | ------- | ----------- |:--------:|
| guildID? | integer | guild ID    |    no    |

| Type     |         |
|----------|---------|
| 0  | None |
| 1  | Low     |
| 2  | Medium    |
| 3  | High     |
| 4  | Highest   |


## Example

This will return the guild's verification Level:

```javascript
bot.command({
  name: 'guildVerificationLevel',
  code: `
  $guildVerificationLevel[$guildID]
  `
});
```

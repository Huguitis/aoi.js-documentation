---
title: $guildEmojis 
description: $guildEmojis will return the emojis of a specific guild.
id: guildEmojis
---

`$guildEmojis` will return the emojis of a specific guild.

## Usage

```php
$guildEmojis[sep?;guildID?]
```

## Parameters 


| Field    | Type    | Description                                   | Required |
| -------- | ------- | --------------------------------------------- |:--------:|
| sep?     | string  | the seperator to seperate the returned emojis |    no    |
| guildID? | integer | guild ID                                      |    no    |


## Example

This will return the emojis of your guild:

```javascript
bot.command({
  name: 'guildEmojis',
  code: `
  $guildEmojis[, ;$guildID]
  `
});
```

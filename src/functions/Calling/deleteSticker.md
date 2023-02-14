---
title: $deleteSticker 
description: $deleteSticker will delete a given sticker.
id: deleteSticker
---

`$deleteSticker` will delete a given sticker.

## Usage

```php
$deleteSticker[guildID;sticker]
```

## Parameters 


| Field   | Type    | Description         | Required |
| ------- | ------- | ------------------- |:--------:|
| guildID | integer | guild ID            |    yes   |
| sticker | string  | name of the sticker |    yes   |


## Example

This will delete a sticker of your guild ( make sure to provide an actual sticker name ):

```javascript
bot.command({
  name: 'deleteSticker',
  code: `
  $deleteSticker[$guildID;sticker]
  `
});
```
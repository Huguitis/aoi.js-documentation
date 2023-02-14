---
title: $createSticker 
description: $createSticker will create a sticker.
id: createSticker
---

`$createSticker` will create a sticker.

## Usage

```php
$createSticker[guildid;url;name;returnSticker?;tags;description;reason]
```

## Parameters 


| Field          | Type    | Description                                                                        | Required |
| -------------- | ------- | ---------------------------------------------------------------------------------- |:--------:|
| guildID        | integer | guild ID                                                                           |    yes   |
| url            | string  | image URL (**png only**)                                                           |    yes   |
| name           | string  | sticker name                                                                       |    yes   |
| returnSticker? | string  | return the sticker after creation <br /> 1. **true** <br /> 2. **false** (default) |    no    |
| tags?          | string  | sticker tags                                                                       |    no    |
| description?   | string  | sticker description                                                                |    no    |
| reason?        | string  | reason that will be displayed in the server's audit logs                           |    no    |


## Example

This will create a sticker called `Imagine`:

```javascript
bot.command({
  name: 'createSticker',
  code: `
  $createSticker[$guildID;https://cdn.discordapp.com/attachments/1061712111052521493/1066397675278323734/692445926480150611.png;Imagine;true;money;Random sticker;Testing.]
  `
});
```

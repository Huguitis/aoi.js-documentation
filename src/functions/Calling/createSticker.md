---
title: $createSticker
description: $createSticker will create a sticker.
id: createSticker
---

`$createSticker` will create a sticker.

## Usage

```php
$createSticker[guildid;URL;name;returnSticker?;tags;description;reason]
```

## Parameters

| Field          | Type    | Description                                                                        | Required |
|----------------|---------|------------------------------------------------------------------------------------|:--------:|
| guildID        | integer | guild ID                                                                           |   true   |
| URL            | string  | image URL (**png only**)                                                           |   true   |
| name           | string  | sticker name                                                                       |   true   |
| returnSticker? | string  | return the sticker after creation <br /> 1. **true** <br /> 2. **false** (default) |  false   |
| tags?          | string  | sticker tags                                                                       |  false   |
| description?   | string  | sticker description                                                                |  false   |
| reason?        | string  | reason that will be displayed in the server's audit logs                           |  false   |

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

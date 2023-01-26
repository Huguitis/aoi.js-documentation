---
title: $attachment 
description: $attachment will create an attachment.
id: attachment
---

`$attachment` will create an attachment.

## Usage

```php
$attachment[attachment;name;type?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| attachment    | string  | attachment                             | yes      |
| name    | string  | attachment name                            | yes      |
| type?    | string  | attachment type <br /> 1. **url** (default)                            | no      |


## Example

This will create an attachment:

```javascript
bot.command({
  name: 'attachment',
  code: `
  $attachment[https://cdn.discordapp.com/emojis/1063432790697328710.webp?size=96&quality=lossless;boost-icon.png;url]
  `
});
```

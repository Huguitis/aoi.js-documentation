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

| Field      | Type   | Description                                 | Required |
|------------|--------|---------------------------------------------|:--------:|
| attachment | string | attachment                                  |   true   |
| name       | string | attachment name                             |   true   |
| type?      | string | attachment type <br /> 1. **URL** (default) |  false   |

## Example

This will create an attachment:

```javascript
bot.command({
    name: 'attachment',
    code: `
  $attachment[https://cdn.discordapp.com/emojis/1063432790697328710.webp?size=96&quality=lossless;boost-icon.png;URL]
  `
});
```

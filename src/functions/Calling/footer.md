---
title: $footer 
description: $footer will add a footer to an embed.
id: footer
---

`$footer` will add a footer to an embed.

## Usage

```php
$footer[index?;text;iconURL?]
```

## Parameters 


| Field    | Type   | Description                     | Required |
| -------- | ------ | ------------------------------- |:--------:|
| index?   | number | embed index/position            |    no    |
| text     | string | content of the footer           |    yes   |
| iconURL? | string | footer Icon (bottom left image) |    no    |

## Example

This will create an embed with a footer and title:

```javascript
bot.command({
  name: 'embed',
  code: `
  $title[Hello!]
  $footer[Hello again!;$userAvatar]
  `
});
```
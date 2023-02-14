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
| index?   | number | embed index/position            |    false    |
| text     | string | content of the footer           |    true   |
| iconURL? | string | footer Icon (bottom left image) |    false    |

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
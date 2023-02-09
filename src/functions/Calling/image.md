---
title: $image 
description: $image will add an image to an embed.
id: image
---

`$image` will add an image to an embed.

## Usage

```php
$image[index?;url]
```

## Parameters 


| Field  | Type   | Description              | Required |
| ------ | ------ | ------------------------ |:--------:|
| index? | number | embed index/position     |    no    |
| url    | string | image (bottom big image) |    yes   |

## Example

This will create an embed with an image, title and footer:

```javascript
bot.command({
  name: 'embed',
  code: `
  $title[Hello!]
  $image[$userAvatar]
  $footer[Hello again!;$userAvatar]
  `
});
```
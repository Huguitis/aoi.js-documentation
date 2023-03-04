---
title: $thumbnail
description: $thumbnail add a thumbnail to an embed (upper right corner image).
id: thumbnail
---

`$thumbnail` add a thumbnail to an embed (upper right corner image).

## Usage

```php
$thumbnail[index?;url]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| index?  | number | embed index        |   false   |
| url  | string | image URL        |   true   |

## Example

This will create an embed with your user avatar in it:

```javascript
bot.command({
    name: 'thumbnail',
    code: `
   $thumbnail[$userAvatar[$authorID]]
   $description[Hello, that's your Avatar!]`
});
```
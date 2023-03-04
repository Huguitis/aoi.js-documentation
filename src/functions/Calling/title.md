---
title: $title
description: $title add a title to an embed.
id: title
---

`$title` add a title to an embed.

## Usage

```php
$title[index?;title;url?]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| index?  | number | embed index        |   false   |
| title  | string | title content        |   true   |
| url?  | string | hyperlink        |   false   |

## Example

This will create an embed with a title:

```javascript
bot.command({
    name: 'title',
    code: `
   $title[Hello!;https://aoi.js.org]
   $description[The title contains a hyperlink..]`
});
```
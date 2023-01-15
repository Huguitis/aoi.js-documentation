---
title: $author 
description: $author will add an author field to an embed.
id: author
---

`$author` will add an author field to an embed.

## Usage

```php
$author[index?;name;iconURL?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| index?    | integer  | embed index                             | no      |
| name    | string  | author title that will be displayed                             | yes      |
| iconURL?   | string  | icon url which will be displayed next to the author title    | no       |


## Example

This will return the amount of roles of your guild:

```javascript
bot.command({
  name: 'author',
  code: `
  $author[Hello!;$userAvatar[$authorID]]
  $description[Embed with author!]
  `
});
```

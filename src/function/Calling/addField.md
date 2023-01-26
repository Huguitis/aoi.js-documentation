---
title: $addField 
description: $addField will add a field in an embed.
id: addField
---

`$addField` will add a field in an embed.

## Usage

```php
$addField[fieldTitle;fieldDescription;inline?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| fieldTitle?    | string  | title                             | yes      |
| fieldDescription?    | string  | description                             | yes      |
| inline?    | string  | inline                             | no      |

## Example

This will return the amount of roles of your guild:

```javascript
bot.command({
  name: 'addField',
  code: `
  $addField[Example;Look at this!;no]
  $description[Hello!]
  `
});
```

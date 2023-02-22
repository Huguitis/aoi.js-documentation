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

| Field             | Type   | Description | Required |
|-------------------|--------|-------------|:--------:|
| fieldTitle?       | string | title       |   true   |
| fieldDescription? | string | description |   true   |
| inline?           | string | inline      |  false   |

## Example

This will send an embed with a field and description:

```javascript
bot.command({
    name: 'addField',
    code: `
  $addField[Example;Look at this!;false]
  $description[Hello!]
  `
});
```

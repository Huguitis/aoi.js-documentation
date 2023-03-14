---
title: $removeContains
description: $removeContains will remove specific text from a give text.
id: removeContains
---

`$removeContains` will remove specific text from a give text.

## Usage

```php
$removeContains[text;...words]
```

## Parameters

| Field    | Type   | Description                         | Required |
|----------|--------|-------------------------------------|:--------:|
| text     | string | text where to remove the words from |   true   |
| ...words | string | word to remove from the text        |   true   |

## Example

This will remove the word "aoi.js from the given text:

```javascript
bot.command({
    name: "removeContains",
    code: `
    $removeContains[Hello, aoi.js!;, ;aoi.js]
    `
});
```
---
title: $cropText
description: $cropText will crop given text.
id: cropText
---

`$cropText` is used to crop given text.

## Usage

```php
$cropText[text;limit;start?]
```

## Parameters

| Field  | Type   | Description                                                             | Required |
|--------|--------|-------------------------------------------------------------------------|----------|
| text   | string | text you want to slice                                                  | true     |
| limit  | number | limit of the cropped text/will start to crop any text coming after that | true     |
| start? | number | where cropping should start                                             | false    |

## Example

This will return `bye` and remove `hello and` from the given text:

```javascript
bot.command({
    name: 'cropText',
    code: `
$cropText[hello and bye;20;9]
  `
});
```

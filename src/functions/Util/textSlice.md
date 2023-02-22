---
title: $textSlice
description: $textSlice will slice a message depending on the given arguments.
id: textSlice
---

`$textSlice` will slice a message depending on the given arguments.

## Usage

```php
$textSlice[text;from?;to]
```

## Parameters

| Field | Type   | Description                               | Required |
|-------|--------|-------------------------------------------|----------|
| text  | string | text you want to slice                    | true     |
| from? | number | starting point where to slice the message | false    |
| to    | number | ending point where slicing ends           | true     |

## Example

This will return `Hello` and remove `Bye` from the given text:

```javascript
bot.command({
    name: 'textSlice',
    code: `
  $textSlice[Hello Bye;0;5]
  `
});
```
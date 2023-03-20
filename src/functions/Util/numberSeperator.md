---
title: $numberseparator
description: $numberseparator will seperate numbers and make them readable.
id: numberseparator
---

`$numberseparator` will seperate numbers and make them readable.

## Usage

```php
$numberseparator[num;sep?]
```

## Parameters

| Field | Type   | Description                                                        | Required |
|-------|--------|--------------------------------------------------------------------|----------|
| num   | number | number you want to seperate                                        | true     |
| sep?  | string | separator which will be used to seperate the numbers, default: `,` | false    |

## Example

This will return `1,000,000`:

```javascript
bot.command({
    name: 'numberseparator',
    code: `
  $numberseparator[1000000;,]
  `
});
```

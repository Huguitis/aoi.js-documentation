---
title: $isValidHex 
description: $isValidHex will check if the given hexadecimal color is valid.
id: isValidHex
---

`$isValidHex` will check if the given hexadecimal color is valid.

## Usage

```php
$isValidHex[color]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| color      | string  | hexadecimal color string                             | yes      |


## Example

This will return `true` as `#30dbd8` is an valid hexadecimal color:

```javascript
bot.command({
  name: 'isValidHex',
  code: `
  $isValidHex[#30dbd8]
  `
});
```

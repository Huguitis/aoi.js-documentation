---
title: $arraySplice
description: $arraySplice will splice elements from the array.
id: arraySplice
---

`$arraySplice` will splice elements from the array.

## Usage

```php
$arraySplice[name;index;amount;...elements]
```

## Parameters

| Field       | Type   | Description          | Required |
|-------------|--------|----------------------|:--------:|
| name        | string | array name           |   true   |
| index       | number | index of the element |   true   |
| amount      | number | amount to splice     |   true   |
| ...elements | string | elements to splice   |   true   |

## Example

```javascript
bot.command({
    name: "array-splice",
    code: `
  $arraySplice[array;2;3]
  $createArray[array;aoi.js;akarui;documents;bot]
  `
});
```
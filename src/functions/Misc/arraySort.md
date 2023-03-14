---
title: $arraySort
description: $arraySort will sort a given array.
id: arraySort
---

`$arraySort` will sort a given array.

## Usage

```php
$arraySort[name;type?]
```

## Parameters

| Field | Type   | Description                                                              | Required |
|-------|--------|--------------------------------------------------------------------------|:--------:|
| name  | string | array name                                                               |   true   |
| type  | string | type to sort after <br /> 1. **asc** (ascending) 2. **dsc** (descending) |   true   |

## Example

```javascript
bot.command({
    name: "array-sort",
    code: `
  $arrayJoin[array;, ]
  $arraySort[array;asc]
  $createArray[array;aoi.js;akarui;documents;bot]
  `
});
```
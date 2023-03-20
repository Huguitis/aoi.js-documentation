---
title: $arrayJoin
description: $arrayJoin will join the array with a given separator.
id: arrayJoin
---

`$arrayJoin` will join the array with a given separator.

## Usage

```php
$arrayJoin[name;separator?]
```

## Parameters

| Field      | Type   | Description | Required |
|------------|--------|-------------|:--------:|
| name       | string | array name  |   true   |
| separator? | string | separator   |  false   |

## Example

```javascript
bot.command({
    name: "array-join",
    code: `
  $arrayJoin[array;, ]
  $createArray[array;aoi.js;akarui;documents;bot]
  `
});
```
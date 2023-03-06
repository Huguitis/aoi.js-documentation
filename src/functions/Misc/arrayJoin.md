---
title: $arrayJoin
description: $arrayJoin will join the array with a given seperator.
id: arrayJoin
---

`$arrayJoin` will join the array with a given seperator.

## Usage

```php
$arrayJoin[name;seperator?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| name      | string   | array name                                                          |   true   |
| seperator?     | string  | seperator |   false   |

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
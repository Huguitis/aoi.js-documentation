---
title: $createArray
description: $createArray will create a new array with given elements.
id: createArray
---

`$createArray` will create a new array with given elements.

## Usage

```php
$createArray[name;...elements]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| name      | string   | array name                                                         |   true   |
| ...elements      | string   | elements to add                                             |   true   |

## Example

```javascript
bot.command({
    name: "array-create",
    code: `
  $createArray[array;aoi.js;akarui;documents;bot]
  `
});
```
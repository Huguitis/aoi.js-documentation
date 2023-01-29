---
title: $arrayAt
description: $arrayAt choose the index (position) of the array element to be returned. Returns nothing if the given index can not be found.
id: arrayAt
---


`$arrayAt` choose the index (position) of the array element to be returned. Returns nothing if the given index can not be found.

## Usage

```php
$arrayAt[name;index]
```

## Parameters 


| Field | Type   | Description                 | Required |
| ----- | ------ | --------------------------- |:--------:|
| name  | string | name of the array           |    yes   |
| index | string | The position of the element |    yes   |

## Example

- This will return `Aoi.dashboard`:

```javascript
bot.command({
  name: "array-at",
  code: `
  $arrayAt[Aoi;3]
  
  $createArray[Aoi;Aoi.music;Aoi.panel;Aoi.dashboard;Aoi]
  `
  // Returns "Aoi.dashboard"
});
```

---
title: $addObjectProperty 
description: $addObjectProperty will create an object in JSON format.
id: addObjectProperty
---

`$addObjectProperty` will create an object in JSON format.

## Usage

```php
$addObjectProperty[name;value]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| name    | string  | name of the propery                             | yes      |
| value     | string  | value of the property          | yes       |


## Example

This will return `Ferel` from the `Leref` Property:

```javascript
bot.command({
  name: 'addObjectProperty',
  code: `
  $getObjectProperty[Leref]
  $addObjectProperty[Leref;Ferel]
  $createObject[{}]
  `
});
```

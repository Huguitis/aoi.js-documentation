---
title: $addObjectProperty
description: $addObjectProperty will add a property to an existing object.
id: addObjectProperty
---

`$addObjectProperty` will add a property to an existing object.

## Usage

```php
$addObjectProperty[name;value]
```

## Parameters

| Field | Type   | Description           | Required |
|-------|--------|-----------------------|:--------:|
| name  | string | name of the propery   |   true   |
| value | string | value of the property |   true   |

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

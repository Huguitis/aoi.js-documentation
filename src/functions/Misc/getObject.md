---
title: $getObject
description: $getObject will return the previously created object.
id: getObject
---

`$getObject` will return the previously created object.

## Usage

```php
$getObject[format?]
```

## Parameters

| Field   | Type   | Description                                                 | Required |
|---------|--------|-------------------------------------------------------------|:--------:|
| format? | string | format the output <br /> 1. **true** (default) 2. **false** |  false   |

## Example

This will return the object created in `$createObject`:

```javascript
bot.command({
    name: "getObject",
    code: `
    $getObject[true]
    $createObject[{"hello": "bye"}]
    `
});
```
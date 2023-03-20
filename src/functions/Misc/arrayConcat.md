---
title: $arrayConcat
description: $arrayConcat will concat two arrays.
id: arrayConcat
---

## Usage

```php
$arrayConcat[separator;name]
```

## Parameters

| Field     | Type   | Description       | Required |
|-----------|--------|-------------------|:--------:|
| separator | string | separator         |   true   |
| name      | string | name of the array |   true   |

## Example

This will return `This is a test`:

```javascript
bot.command({
    name: 'arrayConcat',
    code: `
  $arrayConcat[ ;test;test2]
  $createArray[test;This is]
  $createArray[test2;a test]
  `
});
```

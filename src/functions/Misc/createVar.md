---
title: $createVar
description: $createVar will create a new variable.
id: createVar
---

`$createVar` will create a new variable.

## Usage

```php
$createVar[table;...vars]
```

## Parameters

| Field   | Type   | Description             | Required |
|---------|--------|-------------------------|:--------:|
| table   | string | variable table          |   true   |
| ...vars | string | variable name and value |   true   |

## Example

This will create a new variable with the name of "variable" and the value of "value":

```javascript
bot.command({
    name: "createVar",
    code: `
  $createVar[main;variable;value]
  `
});
```
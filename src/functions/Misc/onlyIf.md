---
title: $onlyIf
description: $onlyIf will check for a condition and return a error message if that condition does not match.
id: onlyIf
---

`$onlyIf` will check for a condition and return a error message if that condition does not match.

## Usage

```php
$onlyIf[condition;error?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| condition    | string, integer, number   | condition to check                                                    |   true   |
| error?    | string   | error to return when condition does not match |   false   |

#### Valid Mathematical Operators

| Operator | Mathematical Expression  |
|----------|--------------------------|
| ==       | equal to                 |
| !=       | not equal to             |
| <=       | less than or equal to    |
| \>=      | greater than or equal to |
| \>       | greater than             |
| <        | less than                |
| \|\|     | logical OR               |
| &&       | logical conjunction      |

## Examples

This will return the error message as 5 does not equal to 3:

```javascript
bot.command({
    name: "onlyIf",
    code: `
    $onlyIf[5==3;That's wrong!]
    `
});
```
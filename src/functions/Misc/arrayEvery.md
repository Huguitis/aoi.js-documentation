---
title: $arrayEvery 
description: $arrayEvery function tests whether all elements in the array pass the condition. It returns boolean value.
id: arrayEvery
---

`$arrayEvery` function tests whether all elements in the array pass the condition. It returns boolean value.


## Usage

```php
$arrayEvery[name;query;queryType?]
```

## Parameters 


| Field     | Type     | Description                                                        | Required |
| --------- | -------- | ------------------------------------------------------------------ |:--------:|
| name      | string   | seperator                                                          |    true   |
| query     | element  | The element we will be queering for every element inside the array |    true   |
| queryType | operator | The comparison operator                                            |    false    |

## Comparison Operators

* `includes` — Including 
* `startsWith` — Starts with
* `endsWith` — Ends with
* `==` — Equal to 
* `!=` — Not equal to
* `>` — Greater than
* `<` — Less than
* `>=` — Greater than or equal to
* `<=` — Less than or equal to

## Example

```javascript
bot.command({
  name: "array-every", 
  code: `
  $arrayEvery[array;30;==]
  $createArray[array;1;2;3;0;30]
  `
  // It will return "false". Cause 1 ≠ 30. You can think it as "and (&&)" logical operator.
});
```

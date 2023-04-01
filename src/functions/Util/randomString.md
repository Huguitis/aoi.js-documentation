---
title: $randomString
description: $randomString will generate a random string.
id: randomString
---

`$randomString` will generate a random string.

## Usage

```php
$randomString[range;diffExec?]
```

## Parameters

| Field     | Type   | Description                          | Required |
|-----------|--------|--------------------------------------|----------|
| range     | number | range of the random generated string | true     |
| diffExec? | string |                                      | false    |

## Example(s)

This will return a random string of twenty characters:

```javascript
bot.command({
    name: 'randomString',
    code: `
  $randomString[20]
  `
});
```

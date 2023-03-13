---
title: $getUserVar
description: $getUserVar will return the value of a given user variable.
id: getUserVar
---

`$getUserVar` will return the value of a given user variable.

## Usage

```php
$getUserVar[varname;userID?;table?]
```

## Parameters

| Field   | Type    | Description    | Required |
|---------|---------|----------------|:--------:|
| varname | string  | variable name  |   true   |
| userID? | integer | user ID        |  false   |
| table?  | string  | variable table |  false   |

## Example

This will return the value of a variable called "Example":

```javascript
bot.command({
    name: "getUserVar",
    code: `
    $getUserVar[Example;$authorID;main]
    `
});
```
---
title: $resetGuildVar
description: $resetGuildVar will set a given guild variable to its default value.
id: resetGuildVar
---

`$resetGuildVar` will set a given guild variable to its default value.

## Usage

```php
$resetGuildVar[varname;table?]
```

## Parameters

| Field   | Type   | Description    | Required |
|---------|--------|----------------|:--------:|
| varname | string | variable name  |   true   |
| table?  | string | variable table |  false   |

## Example

This will reset a variable called "Example":

```javascript
bot.command({
    name: "resetGuildVar",
    code: `
    $resetGuildVar[Example;main]
    `
});
```
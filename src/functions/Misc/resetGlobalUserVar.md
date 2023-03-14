---
title: $resetGlobalUserVar
description: $resetGlobalUserVar will set a given global user variable to its default value.
id: resetGlobalUserVar
---

`$resetGlobalUserVar` will set a given global user variable to its default value.

## Usage

```php
$resetGlobalUserVar[varname;table?]
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
    name: "resetGlobalUserVar",
    code: `
    $resetGlobalUserVar[Example;main]
    `
});
```
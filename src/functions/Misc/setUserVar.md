---
title: $setUserVar
description: $setUserVar will change the value of a given user variable.
id: setUserVar
---

`$setUserVar` will change the value of a given user variable.

## Usage

```php
$setUserVar[varname;value;userID?;id?;table?]
```

## Parameters

| Field   | Type                    | Description                               | Required |
|---------|-------------------------|-------------------------------------------|:--------:|
| varname | string                  | variable name                             |   true   |
| value   | string, integer, number | variable table                            |   true   |
| userID? | integer                 | user ID                                   |  false   |
| id?     | string, integer         | 1. **specific guild id** <br /> 2. **dm** |  false   |
| table?  | string                  | variable table                            |  false   |

## Example(s)

This will change the value of "Example" to "This is a value":

```javascript
bot.command({
    name: "setUserVar",
    code: `
    $setUserVar[Example;This is a value;$authorID;$guildID;main]
    `
});
```
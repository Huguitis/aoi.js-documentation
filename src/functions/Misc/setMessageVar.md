---
title: $setMessageVar
description: $setMessageVar will change the value of a given message variable.
id: setMessageVar
---

`$setMessageVar` will change the value of a given message variable.

## Usage

```php
$setMessageVar[varname;value;messageID?;table?]
```

## Parameters

| Field      | Type                    | Description    | Required |
|------------|-------------------------|----------------|:--------:|
| varname    | string                  | variable name  |   true   |
| value      | string, integer, number | variable table |   true   |
| messageID? | integer                 | message ID     |  false   |
| table?     | string                  | variable table |  false   |

## Example

This will change the value of "Example" to "This is a value":

```javascript
bot.command({
    name: "setMessageVar",
    code: `
    $setMessageVar[Example;This is a value;$messageID;main]
    `
});
```
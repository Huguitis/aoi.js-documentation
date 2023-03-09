---
title: $setGuildVar
description: $setGuildVar will change the value of a given guild variable.
id: setGuildVar
---

`$setGuildVar` will change the value of a given guild variable.

## Usage

```php
$setGuildVar[varname;value;guildID?;table?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| varname    | string   | variable name                                                         |   true   |
| value    | string, integer, number   | variable table                                                         |   true   |
| guildID?    | integer   | guild ID                                                         |   false   |
| table?    | string   | variable table                                                         |   false   |

## Example

This will change the value of "Example" to "This is a value":

```javascript
bot.command({
    name: "setGuildVar",
    code: `
    $setGuildVar[Example;This is a value;$guildID;main]
    `
});
```
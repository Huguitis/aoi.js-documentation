---
title: $getGuildVar
description: $getGuildVar will return the value of a given guild variable.
id: getGuildVar
---

`$getGuildVar` will return the value of a given guild variable.

## Usage

```php
$getGuildVar[varname;guildID?;table?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| varname    | string   | variable name                                                         |   true   |
| guildID?    | integer   | guild ID                                                         |   false   |
| table?    | string   | variable table                                                         |   false   |

## Example

This will return the value of a variable called "Example":

```javascript
bot.command({
    name: "getGuildVar",
    code: `
    $getGuildVar[Example;$guildID;main]
    `
});
```
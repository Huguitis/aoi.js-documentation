---
title: $resetUserVar
description: $resetUserVar will set a given user variable to its default value of a given guild.
id: resetUserVar
---

`$resetUserVar` will set a given user variable to its default value of a given guild.

## Usage

```php
$resetUserVar[varname;guildID?;table?]
```

## Parameters

| Field    | Type    | Description    | Required |
|----------|---------|----------------|:--------:|
| varname  | string  | variable name  |   true   |
| guildID? | integer | guild ID       |  false   |
| table?   | string  | variable table |  false   |

## Example(s)

This will reset a variable called "Example":

```javascript
bot.command({
    name: "resetUserVar",
    code: `
    $resetUserVar[Example;$guildID;main]
    `
});
```
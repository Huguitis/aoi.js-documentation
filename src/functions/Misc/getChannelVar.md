---
title: $getChannelVar
description: $getChannelVar will return the value of a given channel variable.
id: getChannelVar
---

`$getChannelVar` will return the value of a given channel variable.

## Usage

```php
$getChannelVar[varname;channelID?;table?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| varname    | string   | variable name                                                         |   true   |
| channelID?    | integer   | channel ID                                                         |   false   |
| table?    | string   | variable table                                                         |   false   |

## Example

This will return the value of a variable called "Example":

```javascript
bot.command({
    name: "getChannelVar",
    code: `
    $getChannelVar[Example;$channelID;main]
    `
});
```
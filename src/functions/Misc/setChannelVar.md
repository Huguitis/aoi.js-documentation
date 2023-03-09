---
title: $setChannelVar
description: $setChannelVar will change the value of a given channel variable.
id: setChannelVar
---

`$setChannelVar` will change the value of a given channel variable.

## Usage

```php
$setChannelVar[varname;value;channelID?;table?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| varname    | string   | variable name                                                         |   true   |
| value    | string, integer, number   | variable table                                                         |   true   |
| channelID?    | integer   | channel ID                                                         |   false   |
| table?    | string   | variable table                                                         |   false   |

## Example

This will change the value of "Example" to "This is a value":

```javascript
bot.command({
    name: "setChannelVar",
    code: `
    $setChannelVar[Example;This is a value;$channelID;main]
    `
});
```
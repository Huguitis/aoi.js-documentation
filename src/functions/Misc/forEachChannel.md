---
title: $forEachChannel
description: $forEachChannel will execute awaited commands in every channel of every guild.
id: forEachChannel
---

`$forEachChannel` will execute awaited commands in every channel of every guild.

## Usage

```php
$forEachChannel[time;awaitData;...awaitedCmds;endCmd?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| time      | string   | how long it takes between each command to execute the other                                                          |   true   |
| awaitData     | string  | Await Data |   true   |
| awaitedCmds | string | Awaited Commands                                            |  true   |
| endCmd? | string | awaited command to execute when loop ends                                            |  false   |

## Example

This will change the variable value of each channel to "test":

```javascript
bot.command({
    name: "forEachChannel",
    code: `
  $forEachChannel[2s;{"value": "test"};awaitedCommand]
  `
});

bot.awaitedCommand({
    name: "awaitedCommand",
    code: `
  $setChannelVar[varname;$awaitData[value];$channelID]
  `
});
```
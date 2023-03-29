---
title: $forEachGuildChannel
description: $forEachGuildChannel will execute awaited commands in every channel of the current guild.
id: forEachGuildChannel
---

`$forEachGuildChannel` will execute awaited commands in every channel of the current guild.

## Usage

```php
$forEachGuildChannel[time;awaitData;...awaitedCmds;endCmd?]
```

## Parameters

| Field       | Type   | Description                                                 | Required |
|-------------|--------|-------------------------------------------------------------|:--------:|
| time        | string | how long it takes between each command to execute the other |   true   |
| awaitData   | string | Await Data                                                  |   true   |
| awaitedCmds | string | Awaited Commands                                            |   true   |
| endCmd?     | string | awaited command to execute when loop ends                   |  false   |

## Example(s)

This will change the variable value of each guild channel to "test":

```javascript
bot.command({
    name: "forEachGuildChannel",
    code: `
  $forEachGuildChannel[2s;{"value": "test"};awaitedCommand]
  `
});

bot.awaitedCommand({
    name: "awaitedCommand",
    code: `
  $setChannelVar[varname;$awaitData[value];$channelID]
  `
});
```
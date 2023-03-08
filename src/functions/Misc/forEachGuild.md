---
title: $forEachGuild
description: $forEachGuild will execute given awaited commands in every guild.
id: forEachGuild
---

`$forEachGuild` will execute given awaited commands in every guild.

## Usage

```php
$forEachGuild[time;awaitData;...awaitedCmds;endCmd?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| time      | string   | how long it takes between each command to execute the other                                                          |   true   |
| awaitData     | string  | Await Data |   true   |
| awaitedCmds | string | Awaited Commands                                            |  true   |
| endCmd? | string | awaited command to execute when loop ends                                            |  false   |

## Example

This will change the variable value of each guild to "test":

```javascript
bot.command({
    name: "forEachGuild",
    code: `
  $forEachGuild[2s;{"value": "test"};awaitedCommand]
  `
});

bot.awaitedCommand({
    name: "awaitedCommand",
    code: `
  $setGuildVar[varname;$awaitData[value];$guildID]
  `
});
```
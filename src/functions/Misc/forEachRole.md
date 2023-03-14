---
title: $forEachRole
description: $forEachRole will execute awaited commands for every role in a given guild.
id: forEachRole
---

`$forEachRole` will execute awaited commands for every role in a given guild.

## Usage

```php
$forEachRole[guildID;time;awaitData;...awaitedCmds;endCmd?]
```

## Parameters

| Field          | Type   | Description                                                 | Required |
|----------------|--------|-------------------------------------------------------------|:--------:|
| time           | string | how long it takes between each command to execute the other |   true   |
| awaitData      | string | Await Data                                                  |   true   |
| ...awaitedCmds | string | Awaited Commands                                            |   true   |
| endCmd?        | string | awaited command to execute when loop ends                   |  false   |
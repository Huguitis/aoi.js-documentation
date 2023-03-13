---
title: $forEachUser
description: $forEachUser will execute awaited commands for user across all guilds.
id: forEachUser
---

`$forEachUser` will execute awaited commands for user across all guilds.

## Usage

```php
$forEachUser[time;awaitData;...awaitedCmds;endCmd?]
```

## Parameters

| Field          | Type   | Description                                                 | Required |
|----------------|--------|-------------------------------------------------------------|:--------:|
| time           | string | how long it takes between each command to execute the other |   true   |
| awaitData      | string | Await Data                                                  |   true   |
| ...awaitedCmds | string | Awaited Commands                                            |   true   |
| endCmd?        | string | awaited command to execute when loop ends                   |  false   |
---
title: $forEachMember
description: $forEachMember will execute awaited commands for user within the current guild.
id: forEachMember
---

`$forEachMember` will execute awaited commands for user within the current guild.

## Usage

```php
$forEachMember[time;awaitData;...awaitedCmds;endCmd?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| time      | string   | how long it takes between each command to execute the other                                                          |   true   |
| awaitData     | string  | Await Data |   true   |
| ...awaitedCmds | string | Awaited Commands                                            |  true   |
| endCmd? | string | awaited command to execute when loop ends                                            |  false   |
---
title: $forEachUser
description: $forEachUser will execute awaited commands for user across all guilds.
id: forEachUser
---

`$forEachUser` will execute awaited commands for user across all guilds.

## Usage

```php
$forEachUser[time;awaitData;...awaitedCmds;endCmd]
```

## Parameters

| Field          | Type   | Description                                                  | Required |
| -------------- | ------ | ------------------------------------------------------------ | :------: |
| time           | string | How long it takes between each user to execute the next one. |   true   |
| awaitData      | object | Awaited Data.                                                |   true   |
| ...awaitedCmds | string | Awaited Commands to execute.                                 |   true   |
| endCmd         | string | Awaited Command to execute when loop ends.                   |   true   |
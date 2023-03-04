---
title: $removeApplicationCommandPermissions
description: $removeApplicationCommandPermissions will remove permissions of a user or role of a specific application command.
id: removeApplicationCommandPermissions
---

`$removeApplicationCommandPermissions` will remove permissions of a user or role of a specific application command.

## Usage

```php
$pruneMembers[guildID/global;id;roruids]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| guildID/global  | integer | global / guildID        |   true   |
| id  | integer | application command ID        |   true   |
| roruids  | integer, string | roles/users to modify permissions of, splitted by commas        |   true   |
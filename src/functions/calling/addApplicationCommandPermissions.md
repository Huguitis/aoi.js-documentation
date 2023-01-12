---
title: $addApplicationCommandPermissions 
description: $addApplicationCommandPermissions will change permissions of a slash command.
id: addApplicationCommandPermissions
---

## Usage

```php
$addApplicationCommandPermissions[guildID?;id;...perms]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| guildID?       | string  | global or guildID                                          | no      |
| id      | integer  | application command ID                                 | yes      |
| ...perms      | string  | permissions                                 | yes      |

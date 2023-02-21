---
title: $addApplicationCommandPermissions 
description: $addApplicationCommandPermissions will change permissions of a slash command.
id: addApplicationCommandPermissions
---

## Usage

```php
$addApplicationCommandPermissions[guildID/global?;id;...perms]
```

## Parameters 


| Field          | Type    | Description            | Required |
| -------------- | ------- | ---------------------- |:--------:|
| guildID/global | string  | global or guildID      |    true   |
| id             | integer | application command ID |    true   |
| ...perms       | string  | permissions            |    true   |

---
title: $setApplicationCommandPermissions
description: $setApplicationCommandPermissions will set the permissions of a specific application command.
id: setApplicationCommandPermissions
---

`$setApplicationCommandPermissions` will set the permissions of a specific application command.

## Usage

```php
$setApplicationCommandPermissions[guildID/global;ID;...perms]
```

## Parameters 

| Field          | Type            | Description              | Required |
|----------------|-----------------|--------------------------|:--------:|
| guildID/global | integer, string | application command type |   true   |
| ID             | integer         | application command ID   |   true   |
| ...perms       | string          | permissions              |   true   |
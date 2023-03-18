---
title: $modifyApplicationCommand
description: $modifyApplicationCommand will modify an existing application command.
id: modifyApplicationCommand
---

`$modifyApplicationCommand` will modify an existing application command.

## Usage

```php
$modifyApplicationCommand[guildID/global;appID;name:description:type:options:defaultPermission;...options]
```

## Parameters

| Field          | Type            | Description                          | Required |
|----------------|-----------------|--------------------------------------|:--------:|
| guildID/global | integer, string | guildID ID                           |   true   |
| appID          | integer         | application command ID               |   true   |
| ...options     | string          | new data for the application command |   true   |
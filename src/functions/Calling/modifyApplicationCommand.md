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


### [Application Command Option Type](https://discord.com/developers/docs/interactions/application-commands#application-command-object-application-command-option-type)

| NAME              | ID  | NOTE                                                                                         |
|-------------------|-----|----------------------------------------------------------------------------------------------|
| SUB_COMMAND       | 1   |                                                                                              |
| SUB_COMMAND_GROUP | 2   |                                                                                              |
| STRING            | 3   |                                                                                              |
| INTEGER           | 4   | Any Integer between -2^53 and 2^53                                                           |
| BOOLEAN           | 5   |                                                                                              |
| USER              | 6   |                                                                                              |
| CHANNEL           | 7   | Includes all channel types + categories                                                      |
| ROLE              | 8   |                                                                                              |
| MENTIONABLE       | 9   | Includes users and roles                                                                     |
| NUMBER            | 10  | Any double between -2^53 and 2^53                                                            |
| ATTACHMENT        | 11  | [attachment](https://discord.com/developers/docs/resources/channel#attachment-object) object |
---
title: $onlyForGuilds
description: $onlyForGuilds will check if the command was executed in one of the listed guilds and return a error
message if not.
id: onlyForGuilds
---

`$onlyForGuilds` will check if the command was executed in one of the listed guilds and return a error message if not.

## Usage

```php
$onlyForGuilds[...guildIds;error?]
```

## Parameters

| Field       | Type            | Description                                                                   | Required |
|-------------|-----------------|-------------------------------------------------------------------------------|:--------:|
| ...guildIds | string, integer | guilds you want to limit the command to                                       |   true   |
| error?      | string          | error to return when the command was not executed in any of the listed guilds |  false   |

## Examples

This will limit the command only to the listed guilds:

```javascript
bot.command({
    name: "onlyForGuilds",
    code: `
    $onlyForGuilds[guildID;guildID;You can't use that command here!]
    `
});
```
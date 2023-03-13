---
title: $onlyBotPerms
description: $onlyBotPerms will check if the bot has the listed permission and return a error message if not.
id: onlyBotPerms
---

`$onlyBotPerms` will check if the bot has the listed permission and return a error message if not.

## Usage

```php
$onlyBotPerms[...perms;error?]
```

## Parameters

| Field    | Type   | Description                                                 | Required |
|----------|--------|-------------------------------------------------------------|:--------:|
| ...perms | string | permission the bot requires                                 |   true   |
| error?   | string | error to return when the bot has not the listed permissions |  false   |

You can find all permissions __[here](../../guides/9permissionsintents.md)__.

## Examples

This will limit the command to work only when the Bot has administrator permissions:

```javascript
bot.command({
    name: "onlyBotPerms",
    code: `
    $onlyBotPerms[administrator;I don't have administrator permissions!]
    `
});
```
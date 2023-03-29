---
title: $deleteApplicationCommand
description: $deleteApplicationCommand will delete an application command.
id: deleteApplicationCommand
---

`$deleteApplicationCommand` will delete an application command.

## Usage

```php
$deleteApplicationCommand[guildID/global;id]
```

## Parameters

| Field   | Type            | Description        | Required |
|---------|-----------------|--------------------|:--------:|
| guildID | string, integer | guild ID or global |   true   |
| id      | integer         | slash command id   |   true   |

## Example(s)

```javascript
bot.command({
    name: 'deleteApplicationCommand',
    code: `
  $deleteApplicationCommand[$guildID;$getApplicationCommandID[$guildID;slashcommandname]]
  `
});
```

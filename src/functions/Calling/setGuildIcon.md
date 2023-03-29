---
title: $setGuildIcon
description: $setGuildIcon will change a guilds' icon.
id: setGuildIcon
---

`$setGuildIcon` will change a guilds' icon.

## Usage

```php
$setGuildIcon[icon;guildID?]
```

## Parameters

| Field    | Type    | Description    | Required |
|----------|---------|----------------|:--------:|
| icon     | string  | new guild icon |   true   |
| guildID? | integer | guild ID       |  false   |

## Example(s)

This will change guild's icon you're executing the command in to your user avatar:

```javascript
bot.command({
    name: 'setGuildIcon',
    code: `
   $setGuildIcon[$userAvatar[$authorID];$guildID]`
});
```
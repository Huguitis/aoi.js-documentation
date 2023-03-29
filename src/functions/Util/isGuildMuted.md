---
title: $isGuildMuted
description: $isGuildMuted is similar but not to confuse with `$isMuted`, this will check if the user is server muted.
id: isGuildMuted
---

`$isGuildMuted` is similar but not to confuse with `$isMuted`, this will check if the user is server muted.

## Usage

```php
$isGuildMuted[userid?;guildid?]
```

## Parameters

| Field    | Type    | Description                                                       | Required |
|----------|---------|-------------------------------------------------------------------|----------|
| userid?  | integer | the user id of the user you want to check if they're server muted | false    |
| guildid? | integer | the guild id of the guild where they're server muted in           | false    |

## Example(s)

This will return either `true` or `false` depending on if you're server muted or not:

```javascript
bot.command({
    name: 'isGuildMuted',
    code: `
  $isGuildMuted[$authorID;$guildID]
  `
});
```

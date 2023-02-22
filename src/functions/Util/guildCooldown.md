---
title: $guildCooldown
description: $guildCooldown will set a cooldown for the guild after being used.
id: guildCooldown
---

`$guildCooldown` will set a guild-based cooldown.

## Usage

```php
$guildCooldown[time;errorMessage?]
```

* You are able to retrieve the remaining cooldown in the `$guildCooldown` function by using **`%time%`**.

## Parameters

| Field         | Type   | Description                                                | Required |
|---------------|--------|------------------------------------------------------------|----------|
| time          | number | the duration of the cooldown                               | true     |
| errorMessage? | string | error message when there's remaining time for the cooldown | false    |

## Example

This will set a cooldown for a command which applies to the guild only and returns the remaining cooldown:

```javascript
bot.command({
    name: 'guildCooldown',
    code: `
  hello
  $guildCooldown[2m;Please wait %time% to execute this command again.]
  `
});
```

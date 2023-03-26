---
title: $tempCooldown
description: $tempCooldown will create a temporary cooldown for a command.
id: tempCooldown
---

`$tempCooldown` will create a temporary cooldown for a command.

## Usage

```php
$tempCooldown[time;id;errorMessage?]
```

* You are able to retrieve the remaining cooldown in the `$tempCooldown` function by using **`%time%`** or any of the
  following below.
    * `%time%`, `%year%`, `%month%`, `%week%`, `%day%`, `%hour%`, `%min%`, `%sec%`, `%ms%`, `%fullTime%`

## Parameters

| Field         | Type   | Description                                                | Required |
|---------------|--------|------------------------------------------------------------|----------|
| time          | string | the duration of the cooldown                               | true     |
| id            | string | can be user, guild, message, channel or any other ID       | true     |
| errorMessage? | string | error message when there's remaining time for the cooldown | false    |

## Example

This will set a temporary cooldown for a command which applies once only:

```javascript
bot.command({
    name: 'tempCooldown',
    code: `
  hello
  $tempCooldown[2m;customid;Please wait %time% to execute this command again.]
  `
});
```

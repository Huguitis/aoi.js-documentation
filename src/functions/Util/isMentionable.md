---
title: $isMentionable
description: $isMentionable check if a given role is mentionable.
id: isMentionable
---

`$isMentionable` check if a given role is mentionable.

## Usage

```php
$isMentionable[roleID;guildID?]
```

## Parameters

| Field    | Type    | Description                                     | Required |
|----------|---------|-------------------------------------------------|----------|
| roleID   | integer | the role id to check if it's mentionable or not | true     |
| guildID? | integer | guild id where the role is present in           | false    |

## Example

This will check if a role with the name `Owner` is mentionable and returns either `true` or `false`:

```javascript
bot.command({
    name: 'isMentionable',
    code: `
  $isMentionable[$findRole[Owner];$guildID]
  `
});
```

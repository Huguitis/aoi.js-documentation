---
title: $kick
description: $kick will remove a user from a given guild.
id: kick
---

`$kick` will remove a user from a given guild.

## Usage

```php
$kick[userID;guildID?;reason?]
```

## Parameters

| Field    | Type    | Description                                             | Required |
|----------|---------|---------------------------------------------------------|:--------:|
| userID   | integer | user ID                                                 |   true   |
| guildID? | integer | guild ID                                                |  false   |
| reason?  | string  | reason that will be displayed in the guild's audit logs |  false   |

## Example

This will kick someone from your guild:

```javascript
bot.command({
  name: 'kick',
  code: `
  <@$findMember[$message;false]> has been kicked!
  $kick[$findMember[$message;false];$guildID;Example reason!]
  `
});
```

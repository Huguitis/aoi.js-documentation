---
title: $moveUser
description: $moveUser will move a given user between two Voice Channels.
id: moveUser
---

`$moveUser` will move a given user between two Voice Channels.

## Usage

```php
$moveUser[guildID;userID;channelID;reason?]
```

## Parameters 

| Field     | Type    | Description                                | Required |
|-----------|---------|--------------------------------------------|:--------:|
| guildID   | integer | guild ID                                   |   true   |
| userID    | integer | user ID                                    |   true   |
| channelID | integer | voice channel ID                           |   true   |
| reason?   | string  | reason to display in the guilds audit logs |  false   |

## Example

This will move a user to another Voice Channel:

```javascript
bot.command({
    name: 'moveUser',
    code: `
  $moveUser[$guildID;userID;new voice channel ID;Testing!]
  `
});
```
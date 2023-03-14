---
title: $muteUser
description: $muteUser will mute or unmute a given user in a Voice Channel.
id: muteUser
---

`$muteUser` will mute or unmute a given user in a Voice Channel.

## Usage

```php
$muteUser[guildID;userID;mute?;reason?]
```

## Parameters 

| Field   | Type    | Description                                                                     | Required |
|---------|---------|---------------------------------------------------------------------------------|:--------:|
| guildID | integer | guild ID                                                                        |   true   |
| userID  | integer | user ID                                                                         |   true   |
| mute?   | integer | mute or unmute <br /> 1. **true** (mute / default) <br /> 2. **false** (unmute) |  false   |
| reason? | string  | reason to display in the guilds audit logs                                      |  false   |

## Example

This will server mute yourself (must be in a voice channel):

```javascript
bot.command({
    name: 'muteUser',
    code: `
  $muteUser[$guildID;$authorID;true]
  `
});
```
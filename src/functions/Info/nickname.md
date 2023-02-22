---
title: $nickname
description: $nickname will return a user's nickname.
id: nickname
---

`$nickname` will return a user's nickname.

## Usage

```php
$nickname[userID?;guildID?;returnUser?]
```

## Parameters

| Field       | Type    | Description                                                          | Required |
|-------------|---------|----------------------------------------------------------------------|----------|
| guildID?    | integer | id of the guild                                                      | false    |
| userID?     | integer | user ID of the person who you want the nickname of                   | false    |
| returnUser? | string  | return the username <br /> 1. **true** <br /> 2. **false** (default) | false    |

## Example

This will return your nickname, if you have none then it'll return your Discord username as `$nickname` returns nothing
when the user has false nickname:

```javascript
bot.command({
    name: 'nickname',
    code: `
  $replaceText[$replaceText[$checkCondition[$nickname[$authorID;$guildID;true]==];true;$username[$authorID]];false;$nickname[$authorID;$guildID;true]]
  `
});
```

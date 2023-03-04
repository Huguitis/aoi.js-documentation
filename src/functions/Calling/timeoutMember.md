---
title: $timeoutMember
description: $timeoutMember will timeout a given member using Discord's Timeout feature.
id: timeoutMember
---

`$timeoutMember` will timeout a given member using Discord's Timeout feature.

## Usage

```php
$timeoutMember[guildID;memberID;timer;timeoutEndsAt?;reason?]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| guildID  | integer | guild ID        |   true   |
| memberID | integer | member ID        |   true   |
| timer  | string, number | duration        |   true   |
| timeoutEndsAt?  | string | returns time when timeout ends  <br /> 1. **true** <br /> 2. **false** (default)       |   false   |
| reason?  | string | reason that will be displayed in the guild's audit logs        |   false   |

## Example

This will timeout a given member for five minutes:

```javascript
bot.command({
    name: 'timeoutMember',
    code: `
   $timeoutMember[$guildID;userID;5m;false]`
});
```
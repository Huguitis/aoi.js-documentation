---
title: $userPerms
description: $userPerms will return a user's permission of a specific guild.
id: userPerms
---

`$userPerms` will return a user's permission of a specific guild.

## Usage

```php
$userPerms[userID?;sep?;guildID?]
```

## Parameters

| Field    | Type    | Description                              | Required |
|----------|---------|------------------------------------------|:--------:|
| userID?  | integer | user ID                                  |  false   |
| sep?     | string  | separator to separate multiple arguments |  false   |
| guildID? | integer | guild ID                                 |  false   |

## Example

This will return your permissions:

```javascript
bot.command({
    name: 'userPerms',
    code: `
  $userPerms[$authorID;, ;$guildID]
  `
});
```

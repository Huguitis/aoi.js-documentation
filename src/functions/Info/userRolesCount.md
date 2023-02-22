---
title: $userRolesCount
description: $userRolesCount will return a user's role count.
id: userRolesCount
---

`$userRolesCount` will return a user's role count.

## Usage

```php
$userRolesCount[userID?;guildID?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|:--------:|
| userID?  | integer | user ID     |  false   |
| guildID? | integer | guild ID    |  false   |

## Example

This will return the amount of roles you have assigned:

```javascript
bot.command({
    name: 'userRolesCount',
    code: `
  $userRolesCount[$authorID;$guildID]
  `
});
```

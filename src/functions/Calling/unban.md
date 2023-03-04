---
title: $unban
description: $unban will unban a given user.
id: unban
---

`$unban` will unban a given user.

## Usage

```php
$unban[guildID;userID]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| guildID   | integer | guild ID        |   true   |
| userID   | integer | user ID        |   true   |

## Example

This will unban a given user:

```javascript
bot.command({
    name: 'unban',
    code: `
  $unban[$guildID;userID]
  `
});
```
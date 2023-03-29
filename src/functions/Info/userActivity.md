---
title: $userActivity
description: $activity will return a user's activity.
id: userActivity
---

`$userActivity` will return a user's current activity.

## Usage

```php
$userActivity[guildID?;userID?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|----------|
| guildID? | integer | guild id    | false    |
| userID?  | integer | user id     | false    |

## Example(s)

This will return your current Activity:

```javascript
bot.command({
    name: 'useractivity',
    code: `
  $userActivity[$guildID;$authorID]
  `
});
```
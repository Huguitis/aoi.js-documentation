---
title: $userID
description: $userID will return a given user's ID.
id: userID
---

`$userID` will return a given user's ID.

## Usage

```php
$userID[user]
```

## Parameters

| Field | Type   | Description                     | Required |
|-------|--------|---------------------------------|:--------:|
| user  | string | user you want to have the ID of |   true   |

## Example

This will return your user ID:

```javascript
bot.command({
    name: 'userID',
    code: `
  $userID[$username]
  `
});
```

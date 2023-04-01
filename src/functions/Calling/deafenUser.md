---
title: $deafenUser
description: $deafenUser will deafen a user.
id: deafenUser
---

`$deafenUser` will deafen a user.

## Usage

```php
$deafenUser[userID;deaf?]
```

## Parameters

| Field  | Type    | Description                                                                | Required |
|--------|---------|----------------------------------------------------------------------------|:--------:|
| userID | integer | user ID                                                                    |   true   |
| deaf?  | string  | deafen or undeafen a user <br /> 1. **true** (default) <br /> 2. **false** |  false   |

## Example(s)

This will deafen yourself:

```javascript
bot.command({
    name: 'deafen',
    code: `
  $deafen[$authorID;true]
  `
});
```

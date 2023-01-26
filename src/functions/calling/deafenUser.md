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


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| userID    | integer  | user ID                             | yes      |
| deaf?    | string  | deafen or undeafen a user <br /> 1. **yes** (default) <br /> 2. **no**   | no      |


## Example

This will deafen yourself:

```javascript
bot.command({
  name: 'deafen',
  code: `
  $deafen[$authorID;yes]
  `
});
```

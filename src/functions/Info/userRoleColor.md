---
title: $userRoleColor 
description: $userRoleColor will return the role color of your highest assigned role.
id: userRoleColor
---

`$userRoleColor` will return the role color of your highest assigned role.

## Usage

```php
$userRoleColor[userID?;guildID?]
```

## Parameters 


| Field    | Type    | Description | Required |
| -------- | ------- | ----------- |:--------:|
| userID?  | integer | user ID     |    false    |
| guildID? | integer | guild ID    |    false    |


## Example

This will return the color of your highest role:

```javascript
bot.command({
  name: 'userRoleColor',
  code: `
  $userRoleColor[$authorID;$guildID]
  `
});
```

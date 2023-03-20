---
title: $userRoles
description: $userRoles will return the roles of a specific user.
id: userRoles
---

`$userRoles` will return the roles of a specific user.

## Usage

```php
$userRoles[userID?;guildID?;option?;sep?]
```

## Parameters

| Field    | Type    | Description                                                                                  | Required |
|----------|---------|----------------------------------------------------------------------------------------------|:--------:|
| userID?  | integer | user ID                                                                                      |  false   |
| guildID? | integer | guild ID                                                                                     |  false   |
| option?  | string  | how to returnt the roles <br /> 1. **name** (default) <br /> 2. **id** <br /> 3. **mention** |  false   |
| sep?     | string  | separator to seperate multiple arguments                                                     |  false   |

## Example

This will return your roles:

```javascript
bot.command({
    name: 'userRoles',
    code: `
  $userRoles[$authorID;$guildID;id;, ]
  `
});
```

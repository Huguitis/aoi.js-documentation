---
title: $hasAnyRole 
description: $hasAnyRole will check if the provided user has any of the roles listed in the roles argument.
id: hasAnyRole
---

`$hasAnyRole` will check if the provided user has any of the roles listed in the roles argument.

## Usage

```php
$hasAnyRole[guildID;userID;...roles]
```

## Parameters 


| Field   | Type    | Description                             | Required |
| ------- | ------- | --------------------------------------- | -------- |
| guildID | integer | guild ID where the roles are present in | true      |
| userID  | integer | user ID of the user which has the roles | true      |
| roles   | integer | the roles that will be checked for      | true      |


## Example

This will return `true` when the user has any of the listed roles:

```javascript
bot.command({
  name: 'hasAnyRole',
  code: `
  $hasAnyRole[$guildID;$authorID;$findRole[Owner];$findRole[Admin]]
  `
});
```

---
title: $username 
description: $username will return a user's username.
id: username
---

`$username` will return a user's username.

## Usage

```php
$username[userID?]
```

## Parameters 


| Field   | Type    | Description | Required |
| ------- | ------- | ----------- |:--------:|
| userID? | integer | user ID     |    false    |


## Example

This will return your username:

```javascript
bot.command({
  name: 'username',
  code: `
  $username[$authorID]
  `
});
```

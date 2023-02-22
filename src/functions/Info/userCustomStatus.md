---
title: $userCustomStatus
description: $userCustomStatus will return a user's custom status.
id: userCustomStatus
---

`$userCustomStatus` will return a user's custom status.

## Usage

```php
$userCustomStatus[userID?;guildID?;method?]
```

## Parameters

| Field    | Type    | Description                                                                                                                        | Required |
|----------|---------|------------------------------------------------------------------------------------------------------------------------------------|:--------:|
| userID?  | integer | user ID                                                                                                                            |  false   |
| guildID? | integer | guild ID                                                                                                                           |  false   |
| method?  | string  | which part of the status to return <br /> 1. **state** (default) - returns the status text <br /> 2. **emoji** - returns the emoji |  false   |

## Example

This will return your status text if you have any:

```javascript
bot.command({
    name: 'userCustomStatus',
    code: `
  $userCustomStatus[$authorID;$guildID;state]
  `
});
```

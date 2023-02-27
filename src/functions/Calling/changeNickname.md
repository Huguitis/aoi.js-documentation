---
title: $changeNickname
description: $changeNickname will change a nickname of a guild member.
id: changeNickname
---

`$changeNickname` will change a nickname of a guild member.

## Usage

```php
$changeNickname[userID;nick;reason?]
```

## Parameters

| Field   | Type    | Description                                               | Required |
|---------|---------|-----------------------------------------------------------|:--------:|
| userID  | integer | user ID                                                   |   true   |
| nick    | integer | new nickname                                              |   true   |
| reason? | integer | reason which will be displayed in the server's audit logs |  false   |

## Example

This will change your nickname to "I love aoi.js": (wont work if you're the guild owner)

```javascript
bot.command({
    name: 'changeNickname',
    code: `
  $changeNickname[$authorID;I love aoi.js;They simply love aoi.js]
  `
});
```

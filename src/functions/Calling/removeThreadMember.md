---
title: $removeThreadMember
description: $removeThreadMember will remove a given thread member from a given thread.
id: removeThreadMember
---

`$removeThreadMember` will remove a given thread member from a given thread.

## Usage

```php
$removeThreadMember[channelID;threadID;userID;reason?]
```

## Parameters

| Field     | Type    | Description                                | Required |
|-----------|---------|--------------------------------------------|:--------:|
| channelID | integer | channel ID                                 |   true   |
| threadID  | integer | thread ID                                  |   true   |
| userID    | integer | user ID                                    |   true   |
| reason?   | string  | reason to display in the guilds audit logs |  false   |

## Example(s)

This will remove the command author from a given thread:

```javascript
bot.command({
    name: 'removeThreadMember',
    code: `
   $removeThreadMember[$channelID;threadID;$authorID;Testing functions!]
  `
});
```
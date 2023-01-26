---
title: $addThreadMember 
description: $addThreadMember will add a member to a thread.
id: addThreadMember
---

`$addThreadMember` will add a member to a thread.

## Usage

```php
$addThreadMember[channelID;threadID;userID;reason]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| channelID    | integer  | channel ID                             | yes      |
| threadID    | integer  | thread ID                             | yes      |
| userID    | integer  | user id                             | yes      |
| reason    | string  | reason to display in audit logs                             | yes      |


## Example

This will create a thread and a random user to it:

```javascript
bot.command({
  name: 'addThreadMember',
  code: `
  $addThreadMember[$channelID;$get[id];$randomUserID;testing]
  $let[id;$createThread[$channelID;example;1440;public;$messageID;yes]]  
  `
});
```

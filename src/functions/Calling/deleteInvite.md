---
title: $deleteInvite 
description: $deleteInvite will delete a specific guild invite.
id: deleteInvite
---

`$deleteInvite` will delete a specific guild invite.

## Usage

```php
$deleteInvite[guildID;inviteCode;reason?]
```

## Parameters 


| Field      | Type    | Description                                             | Required |
| ---------- | ------- | ------------------------------------------------------- |:--------:|
| guildID    | integer | guild ID                                                |    yes   |
| inviteCode | string  | invite code                                             |    yes   |
| reason?    | string  | reason that will be displayed in the guild's audit logs |    no    |


## Example

This will delete an invite (wont work as the invite code doesnt exit):

```javascript
bot.command({
  name: 'deleteInvite',
  code: `
  $deleteInvite[$guildID;ifawd9a;Testing!]
  `
});
```
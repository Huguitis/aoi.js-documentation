---
title: $ban 
description: $ban will ban a user of a guild.
id: ban
---

`$ban` will ban a user of a guild.

## Usage

```php
$ban[guildID?;userID;days?;reason?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| guildID?    | integer  | guild ID                             | no      |
| userID    | integer  | user ID to ban                             | yes      |
| days?    | string  | days of message history to delete, cannot be higher than 14 days | no      |
| reason?    | string  | ban reason                             | no      |


## Example

This will ban a random user of your guild:

```javascript
bot.command({
  name: 'ban',
  code: `
  $ban[$guildID;$randomUserID;7;Imagine getting banned.]
  `
});
```

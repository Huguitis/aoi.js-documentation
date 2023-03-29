---
title: $status
description: $status will a user's presence.
id: status
---

`$status` will a user's presence.

## Usage

```php
$status[userId?;guildId?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|:--------:|
| userId?  | integer | user ID     |  false   |
| guildId? | integer | guild ID    |  false   |

## Example(s)

This will either return `idle`, `online`, `invisible` or `dnd` depending on your current presence:

```javascript
bot.command({
    name: 'status',
    code: `
  $status[$authorID;$guildID]
  `
});
```

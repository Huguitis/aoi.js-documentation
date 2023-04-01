---
title: $botOwnerID
description: $botOwnerID will return the user IDs of the bot owner (or of multiple people if you have a team).
id: botOwnerID
---

`$botOwnerID` will return the user IDs of the bot owner (or of multiple people if you have a team).

## Usage

```php
$botOwnerID[separator?]
```

## Parameters

| Field      | Type   | Description                                 | Required |
|------------|--------|---------------------------------------------|:--------:|
| separator? | string | separator to split user ids (default: `, `) |  false   |

## Example(s)

This will return your user ID:

```javascript
bot.command({
    name: 'botOwnerID',
    code: `
  $botOwnerID
  `
});
```
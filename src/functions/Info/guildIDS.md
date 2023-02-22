---
title: $guildIDS
description: $guildIDS will return the ID of every guild your bot is in.
id: guildIDS
---

`$guildIDS` will return the ID of every guild your bot is in.

## Usage

```php
$guildIDS[sep?]
```

## Parameters

| Field | Type   | Description                                 | Required |
|-------|--------|---------------------------------------------|:--------:|
| sep?  | string | the seperator to seperate multiple argument |  false   |

## Example

This will return all guild IDs your bot is in:

```javascript
bot.command({
    name: 'guildIDS',
    code: `
  $guildIDS[, ]
  `
});
```

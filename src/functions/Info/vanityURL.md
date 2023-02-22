---
title: $vanityURL
description: $vanityURL will return a guild's vanity URL.
id: vanityURL
---

`$vanityURL` will return a guild's vanity URL.

## Usage

```php
$vanityURL[guildID?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|:--------:|
| guildID? | integer | guild ID    |  false   |

## Example

This will return the vanity URL of your guild, if you have one:

```javascript
bot.command({
    name: 'vanityURL',
    code: `
  $vanityURL[$guildID]
  `
});
```

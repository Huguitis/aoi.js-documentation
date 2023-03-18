---
title: $broadcastEval
description: $broadcastEval will execute a code in all guilds of all shards.
id: broadcastEval
---

`$broadcastEval` will execute a code in all guilds of all shards. (requires sharding)

## Usage

```php
$broadcastEval[func]
```

## Parameters

| Field | Type   | Description              | Required |
|-------|--------|--------------------------|:--------:|
| func  | string | function or code to eval |   true   |

## Example

**Requires Sharding - Review the Sharding Guide if you need explanation**

This will return the amount of servers your bot is in:

```javascript
bot.command({
    name: 'broadcastEval',
    code: `
  $broadcastEval[$guildCount]
  `
});
```

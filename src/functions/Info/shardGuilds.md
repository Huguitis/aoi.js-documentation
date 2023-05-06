---
title: $shardGuilds
description: $shardGuilds will return the guilds of a specific shard.
id: shardGuilds
---

`$shardGuilds` will return the guilds of a specific shard.

## Usage

```php
$shardGuilds[option?;sep?;shardId]
```

## Parameters

| Field   | Type    | Description                                                                  | Required |
| ------- | ------- | ---------------------------------------------------------------------------- | :------: |
| option? | integer | Option to return the guilds in <br /> 1. **id** (default) <br /> 2. **name** |  false   |
| sep?    | string  | Separator to separate multiple returned values.                              |  false   |
| shardId | integer | The shard ID.                                                                |   true   |

#### Note that this won't work without sharding. If you're unsure, review the [sharding guide](../../guides/7sharding.md).

## Example(s)

This will return the amount guilds of a shard:

```javascript
bot.command({
    name: 'shardGuilds',
    code: `
  $shardGuilds[name;, ;$shardID]
  `
});
```

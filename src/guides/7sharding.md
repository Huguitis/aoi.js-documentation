---
title: Sharding
description: This Guide will be covering how to integrate Sharding for your Discord Bot.
id: sharding
---

## Introduction

aoi.js has `ClientShard` class to handle `Sharding` for your Discord Bot.

## Usage

```ts
const sharder: ClientShard = new ClientShard(
    file
:
string,
    sharderOptions ? : ShardOption,
    spawnOptions ? : SpawnOption
)
```

### File Parameters

<table>
  <tr>
    <th>Type</th>
    <td>string</td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Path to bot file</td>
  </tr>
    <tr>
    <th>Required</th>
    <td>true</td>
  </tr>
  <tr>
    <th>Default</th>
    <td>N/A</td>
  </tr>
</table>

### sharderOptions

| Property         | Type      | Description                          | Required                               | Default          |
|------------------|-----------|--------------------------------------|----------------------------------------|------------------|
| **_totalShard_** | string \  | number                               | number of total Shards                 | false            | auto    |
| **_shardList_**  | string \  | number[]                             | List of Shards to spawn                | false            | auto    |
| **_mode_**       | process \ | worker                               | type of Sharding Mode (child_process \ | worker_threads ) | false       | process |
| **_respawn_**    | boolean   | whether to respawn shards on exiting | false                                  | true             |
| token            | string    | token to use for shard count         | false                                  | none             |

### spawnOptions

| Property      | Type     | Description                                                                     | Required                  | Default |
|---------------|----------|---------------------------------------------------------------------------------|---------------------------|---------|
| **_amount_**  | string \ | number                                                                          | number of shards to spawn | false   | `ClientShard#totalShards` |
| **_delay_**   | number   | delay for spawning each shard ( `in ms` )                                       | false                     | 5500    |
| **_timeout_** | number   | The amount in milliseconds to wait until the `Bot` has become ready ( `in ms` ) | false                     | 30000   |

## Example

This should be a new file, for example `shard.js`:

```js
const {ClientShard} = require("aoi.js");

const sharder = new ClientShard("./index.js", {
    token: "DISCORD BOT TOKEN"
});


sharder.startProcess();
```

This is is your main file which is the source running your Discord Bot, it's typically your `index.js`:

```js
const { AoiClient } = require("aoi.js");
const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["Guilds", "GuildMessages", "MessageContent"],
    events: ["onMessage"]
});

bot.command({
    name: "ping",
    code: `
        Pong!
        WS -> $ping ms
        ShardId -> $shardId
        ShardPing -> $shardPing[$shardId]
    `,
});
```

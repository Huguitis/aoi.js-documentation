---
title: onGuildUpdate
description: Emitted whenever a guild updates, gets modified.
id: onGuildUpdate
---

This event will be emitted whenever a guild updates, gets modified.

```javascript
const { AoiClient, LoadCommands } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages"],
    events: ["onMessage", "onInteractionCreate", "onGuildUpdate"]
});
```

### Example Usage

```javascript
module.exports = [{
    type: "guildUpdate",
    channel: "channel ID",
    code: `
    $channelSendMessage[channelID;Something changed here!]
    `
}]
```
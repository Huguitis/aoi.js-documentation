---
title: onGuildLeave
description: Emitted whenever the bot leaves a guild.
id: onGuildLeave
---

This event will be emitted whenever the bot leaves a guild.

```javascript
const { AoiClient, LoadCommands } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages"],
    events: ["onMessage", "onInteractionCreate", "onGuildLeave"]
});
```

### Example Usage

```javascript
module.exports = [{
    type: "guildLeave",
    channel: "channel ID",
    code: `
    $channelSendMessage[channelID;I left a guild!]
    `
}]
```
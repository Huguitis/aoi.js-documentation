---
title: onGuildJoin
description: Emitted whenever the bot joins a guild.
id: onGuildJoin
---

This event will be emitted whenever the bot joins a guild.

```javascript
const { AoiClient } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages"],
    events: ["onMessage", "onInteractionCreate", "onGuildJoin"]
});
```

### Example Usage

```javascript
module.exports = [{
    type: "guildJoin",
    channel: "channel ID",
    code: `
    $channelSendMessage[channelID;I joined a new guild!]
    `
}]
```
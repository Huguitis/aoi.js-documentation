---
title: onGuildUnavailable
description: Emitted whenever a guild becomes unavailable.
id: onGuildUnavailable
---

This event will be emitted whenever a guild becomes unavailable.

```javascript
const { AoiClient } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages"],
    events: ["onMessage", "onInteractionCreate", "onGuildUnavailable"]
});
```

### Example Usage

```javascript
module.exports = [{
    type: "guildUnavailable",
    channel: "channel ID",
    code: `
    $channelSendMessage[channelID;Some guild is unavailable!]
    `
}]
```
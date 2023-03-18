---
title: onMessageDelete
description: Emitted whenever a message is deleted.
id: onMessageDelete
---

This event will be emitted whenever a message is deleted.

```javascript
const { AoiClient, LoadCommands } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages"],
    events: ["onMessage", "onInteractionCreate", "onMessageDelete"]
});

const loader = new LoadCommands(bot);
loader.load(bot.cmd, "./commands/") // you can change this to any directory you want
```

### Example Usage

```javascript
module.exports = [{
    type: "messageDelete",
    channel: "$channelID",
    code: `
    "$message" was deleted by $userTag[$authorID]
    `
}]
```
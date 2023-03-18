---
title: onReactionRemove
description: Emitted whenever a reaction is removed from a message.
id: onReactionRemove
---

This event will be emitted whenever a reaction is removed from a message.

```javascript
const { AoiClient, LoadCommands } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages", "GuildMessageReactions"],
    events: ["onMessage", "onInteractionCreate", "onReactionRemove"]
});

const loader = new LoadCommands(bot);
loader.load(bot.cmd, "./commands/") // you can change this to any directory you want
```

### Example Usage

```javascript
module.exports = [{
    type: "reactionRemove",
    channel: "$channelID",
    code: `
    $userTag[$authorID] removed a reaction from $messageURL
    `
}]
```
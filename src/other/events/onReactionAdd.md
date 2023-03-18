---
title: onReactionAdd
description: Emitted whenever a reaction is added to a message.
id: onReactionAdd
---

This event will be emitted whenever a reaction is added to a message.

```javascript
const { AoiClient, LoadCommands } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages", "GuildMessageReactions"],
    events: ["onMessage", "onInteractionCreate", "onReactionAdd"]
});

const loader = new LoadCommands(bot);
loader.load(bot.cmd, "./commands/") // you can change this to any directory you want
```

### Example Usage

```javascript
module.exports = [{
    type: "reactionAdd",
    channel: "$channelID",
    code: `
    $userTag[$authorID] added a reaction to $messageURL
    `
}]
```
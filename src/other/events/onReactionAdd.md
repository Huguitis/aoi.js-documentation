---
title: onReactionAdd
description: Emitted whenever a reaction is added to a message.
id: onReactionAdd
---

This event will be emitted whenever a reaction is added to a message.

```javascript
const { AoiClient } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages", "GuildMessageReactions"],
    events: ["onMessage", "onInteractionCreate", "onReactionAdd"]
});
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
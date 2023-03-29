---
title: onMessageUpdate
description: Emitted whenever a message is updated.
id: onMessageUpdate
---

This event will be emitted whenever a message is updated.

```javascript
const { AoiClient } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages"],
    events: ["onMessage", "onInteractionCreate", "onMessageUpdate"]
});
```

### Example Usage

- `$oldMessage` can be used to retrieve the old message from the client's cache.
- `$message` can be used to return the new message.

```javascript
module.exports = [{
    type: "messageUpdate",
    channel: "$channelID",
    code: `
    $userTag[$authorID] edited "$oldMessage" to "$message"
    `
}]
```
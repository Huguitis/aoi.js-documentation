---
title: alwaysExecute
description: Emitted whenever a message is sent.
id: alwaysExecute
---

This "function" will be emitted whenever a message is sent.

```javascript
const { AoiClient } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages"],
    events: ["onMessage", "onInteractionCreate"]
});
```

### Example Usage

```javascript
module.exports = [{
    name: "$alwaysExecute",
    code: `
    Hello!
`
}]
```
---
title: onRoleUpdate
description: Emitted whenever a role is updated.
id: onRoleUpdate
---

This event will be emitted whenever a role is updated.

```javascript
const { AoiClient } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages", "GuildMessageReactions"],
    events: ["onMessage", "onInteractionCreate", "onRoleUpdate"]
});
```

### Example Usage

- `$oldRole` / `$newRole` can be used to retrieve data about the updated role.

    - **createdTimestamp** &rarr; Will return the createdTimestamp of the role.
    - **createdAt** &rarr; Will return createdAt of the role.
    - **hexColor** &rarr; Will return the hex color of the updated role.
    - **managed** &rarr; Will return true or false whenever the role is managed or not. 
    - **position** &rarr; Will return the role's position. 
    - **permissions** &rarr; Will return the role's permissions.
    - **name** &rarr; Will return the role's name.


```javascript
module.exports = [{
    type: "roleUpdate",
    channel: "$channelID",
    code: `
    $newRole[name] was updated!
    `
}]
```
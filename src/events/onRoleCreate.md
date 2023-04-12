---
title: onRoleCreate
description: Emitted whenever a role is created.
id: onRoleCreate
---

This event will be emitted whenever a role is created.

```javascript
const { AoiClient } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages", "GuildMessageReactions"],
    events: ["onMessage", "onInteractionCreate", "onRoleCreate"]
});
```

### Example Usage

- `$oldRole` / `$newRole` can be used to retrieve data about the created role.

    - **createdTimestamp** &rarr; Will return the createdTimestamp of the role.
    - **id** &rarr; Will return the role's ID.
    - **createdAt** &rarr; Will return createdAt of the role.
    - **hexColor** &rarr; Will return the hex color of the created role.
    - **managed** &rarr; Will return true or false whenever the role is managed or not. 
    - **hoist** &rarr; Will return true or false whenever the role is hoisted or not. 
    - **position** &rarr; Will return the role's position. 
    - **permissions** &rarr; Will return the role's permissions.
    - **name** &rarr; Will return the role's name.

```javascript
module.exports = [{
    type: "roleCreate",
    channel: "$channelID",
    code: `
    $newRole[name] was created!
    `
}]
```

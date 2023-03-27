---
title: onMessageDeleteBulk
description: Emitted whenever messages are deleted in bulk.
id: onMessageDeleteBulk
---

This event will be emitted whenever messages are deleted in bulk.

```javascript
const { AoiClient, LoadCommands } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["MessageContent", "Guilds", "GuildMessages"],
    events: ["onMessage", "onInteractionCreate", "onMessageDeleteBulk"]
});
```

### Example Usage

- `$bulk` can be used to retrieve data about the deleted messages.

    - **messages** &rarr; Will return the deleted messages.
    - **ids** &rarr; Will return the message IDs.
    - **createdTimestamp** &rarr; Will return the createdTimestamp of the deleted messages.
    - **createdAt** &rarr; Will return createdAt of the deleted messages.
    - **userIds** &rarr; Will return the user Ids of the users who sent the deleted messages.
    - **usernames** &rarr; Will return the usernames of the users who sent the deleted messages. 
    - **userTags** &rarr; Will return the username and discriminator who sent the deleted messages. 
    - **userMentions** &rarr; Will return the user mention of the users who sent the deleted messages. 
    - **guildID** &rarr; Will return the guild ID of where the messages got deleted from.
    - **guildName** &rarr; Will return the guild name of where the messages got deleted from.
    - **channelID** &rarr; Will return the channel ID of where the messages got deleted from.
    - **channelName** &rarr; Will return the channel name of where the messages got deleted from.

```javascript
module.exports = [{
    type: "messageDeleteBulk",
    channel: "$channelID",
    code: `
    $title[Bulk Messages!]
    $description[$bulk[messages]]
    `
}]
```
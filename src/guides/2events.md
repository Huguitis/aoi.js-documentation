---
title: Client Events
description: This guide will be covering everything you need to know about events and their usage.
id: events
---

## Using Events

### Table of Content

- **[Understanding Events][1]**
- **[Types of Events][2]**
    - **[Message Based-Events][2.1]**
    - **[Guild Based-Events][2.2]**
    - **[Guild Members Based-Events][2.3]**
    - **[User Based-Events][2.4]**
    - **[Custom Events][2.5]**
- **[Example Usage][3]**

---

**aoi.js** has various event listeners, known as "events", that cater to the majority of events provided by the Discord
API.

Each of them has its own usage and command type for executing specific tasks (for example, for logging purposes).

The events are not mandatory, apart from **`onMessage`** (which is required for the bot to read and send messages), but
if you wish to utilise them, they must be included in your main file, in order for the bot to listen for those events.
This is necessary in order to make use of the different command types.

It's worth bearing in mind that in order to utilise certain events, you'll need to activate your intents on the Discord
Developer Portal.

## Types of Events

### Message Based-Events

* **onMessage** &rarr; (requires **[message content intent](https://discord.com/developers/docs/topics/gateway#caveats)**) Emitted whenever a message is sent.
* **onMessageDelete** &rarr; Emitted whenever a message is deleted.
* **onMessageUpdate** &rarr; Emitted whenever a message is updated (for example, embed or content change).
    - `$oldMessage` &rarr; Retrieves the old message from the client's cache. (if any)
    - `$message` &rarr; Retrieves the new message. (if any)
* **onMessageDeleteBulk** &rarr; Emitted whenever messages are deleted in bulk.
* **onReactionAdd** &rarr; Emitted whenever a reaction is added to a message.
* **onReactionRemove** &rarr; Emitted whenever a reaction is removed from a message.
* **onReactionRemoveAll** &rarr; Emitted whenever all reactions are removed from a message.
* **onReactionRemoveEmoji** &rarr; Emitted when a bot removes an emoji reaction from a cached message.

### Guild Based-Events

* **onGuildJoin** &rarr; Emitted whenever the client joins a guild.
* **onGuildLeave** &rarr; Emitted whenever the client leaves a guild.
* **onGuildUpdate** &rarr; Emitted whenever a guild gets updated (for example, name change).
    * `$oldGuild[option?]` &rarr; Retrieves data of the old guild. (if any)
    * `$newGuild[option?]` &rarr; Retrieves data of the new/updated guild. (if any)
* **onGuildUnavailable** &rarr; Emitted whenever a guild becomes unavailable, likely due to a server outage.
* **onRoleCreate** &rarr; Emitted whenever a role is created.
* **onRoleUpdate** &rarr; Emitted whenever a role gets updated (for example, color change).
    * `$oldRole[option?]` &rarr; Retrieves data of the old role. (if any)
    * `$newRole[option?]` &rarr; Retrieves data of the new/updated role. (if any)
* **onRoleDelete** &rarr; Emitted whenever a role is deleted.
* **onChannelCreate** &rarr; Emitted whenever a channel is created.
* **onChannelUpdate** &rarr; Emitted whenever a channel gets updated. (for example, topic change).
    * `$oldChannel[option?]` &rarr; Retrieves data of the old channel. (if any)
    * `$newChannel[option?]` &rarr; Retrieves data of the new/updated channel. (if any)
* **onChannelDelete** &rarr; Emitted whenever a channel is deleted.
* **onChannelPinsUpdate** &rarr; Emitted whenever the pins of a channel are updated.
* **onStageInstanceCreate** &rarr; Emitted whenever a stage instance is created.
* **onStageInstanceUpdate** &rarr; Emitted whenever a stage instance gets updated.
* **onStageInstanceDelete** &rarr; Emitted whenever a stage instance is deleted.
* **onThreadCreate** &rarr; Emitted whenever a thread is created.
* **onThreadUpdate** &rarr; Emitted whenever a thread gets updated.
* **onThreadDelete** &rarr; Emitted whenever a thread is deleted.
* **onThreadListSync** &rarr; Emitted whenever the client user gains access to a text or news channel that contains
  threads.
* **onThreadMemberUpdate** &rarr; Emitted whenever the client user's thread member is updated.
* **onThreadMembersUpdate** &rarr; (requires **[guild members intent](https://discord.com/developers/docs/topics/gateway#caveats)**) Emitted whenever members are
  added or removed from a thread.
* **onEmojiCreate** &rarr; Emitted whenever a custom emoji is created in a guild.
* **onEmojiDelete** &rarr; Emitted whenever a custom emoji is deleted in a guild.
* **onEmojiUpdate** &rarr; Emitted whenever a custom guild emoji is updated.
    * `$oldEmoji[option?]` &rarr; Retrieves data of the old emoji. (if any)
    * `$newEmoji[option?]` &rarr; Retrieves data of the new emoji. (if any)
* **onStickerCreate** &rarr; Emitted whenever a custom sticker is created in a guild.
* **onStickerDelete** &rarr; Emitted whenever a custom sticker gets deleted in a guild.
* **onStickerUpdate** &rarr; Emitted whenever a custom sticker is updated in a guild.
    * `$oldEmoji[option?]` &rarr; Retrieves data of the old sticker. (if any)
    * `$newEmoji[option?]` &rarr; Retrieves data of the new sticker. (if any)
* **onBanAdd** &rarr; Emitted whenever a member is banned from a guild.
* **onBanRemove** &rarr; Emitted whenever a member is unbanned from a guild.
* **onVoiceStateUpdate** &rarr; Emitted whenever a user changes voice state (for example, joins/leaves a channel,
  mutes/unmutes).
    * `$oldState[option?]` &rarr; Retrieves data of the old voice state. (if any)
    * `$newState[option?]` &rarr; Retrieves data of the new voice state. (if any)
* **onWebhookUpdate** &rarr; Emitted whenever a channel has its webhooks changed.

### Guild Members Based-Events

* **onJoin** &rarr; Emitted whenever a user joins a guild.
* **onLeave** &rarr; Emitted whenever a member leaves a guild, or is kicked.
* **onMemberUpdate** &rarr; Emitted whenever a guild member changes (for example, new role, removed role, nickname).
    * `$oldMember[option?]` &rarr; Retrieves data of the old member. (if any)
    * `$newMember[option?]` &rarr; Retrieves data of the new/updated member. (if any)
* **onMemberAvailable** &rarr; Emitted whenever a member becomes available in a large guild.
* **onMembersChunk** &rarr; Emitted whenever a chunk of guild members is received (all members come from the same
  guild).

### User Based-Events

* **onPresenceUpdate** &rarr; Emitted whenever a guild member's presence changes, or they change one of their details.
    * `$oldPresence[option]` &rarr; Retrieves data of the old presence. (if any)
    * `$newPresence[option]` &rarr; Retrieves data of the new presence. (if any)
* **onTypingStart** &rarr; Emitted whenever a user starts typing in a channel.
* **onUserUpdate** &rarr; Emitted whenever a user's details (for example, username) are changed.
    * `$oldUser[option]` &rarr; Retrieves data of the old user. (if any)
    * `$newUser[option]` &rarr; Retrieves data of the updated/new user. (if any)

### Custom Events

* **onInteractionCreate** &rarr; Emitted whenever a Interaction is created.
* **onApplicationCmdDelete** &rarr; Emitted whenever a Application Command gets deleted.
* **onApplicationCmdUpdate** &rarr; Emitted whenever a Application Command gets updated (for example, name).
    * `$oldApplicationCmd[option?]` &rarr; Retrieves data of the old application command.
    * `$newApplicationCmd[option?]` &rarr; Retrieves data of the updated application command.
* **onVariableCreate** &rarr; Emitted whenever a variable is created.
* **onVariableDelete** &rarr; Emitted whenever a variable gets deleted.
* **onVariableUpdate** &rarr; Emitted whenever a variable gets updated.
    * `$oldVariable[opt;separator?]` &rarr; Retrieves the old data of the variable. (if any)
    * `$newVariable[opt;separator?]` &rarr; Retrieves the new/updated data of the variable. (if any)
* **onShardDisconnect** &rarr; Emitted whenever the client's shard disconnects.
* **onShardError** &rarr; Emitted whenever a shard of the client returns an error.
* **onShardReady** &rarr; Emitted whenever a shard of the client is ready.
* **onShardReconnecting** &rarr; Emitted whenever a shard of the client is currently reconnecting.
* **onShardResume** &rarr; Emitted whenever the shard resumed operations.

## Example Usage of Events

```js
const { AoiClient } = require("aoi.js");

const bot = new AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["Guilds", "GuildMessages", "MessageContent"],
    events: ["onMessage", "onJoin", "onLeave", "onBanAdd", "onBanRemove"]
    ...
});
```

<!--- links -->

[1]: #table-of-content
[2]: #types-of-events
[2.1]: #message-based-Events
[2.2]: #guild-based-events
[2.3]: #guild-members-based-events
[2.4]: #user-based-events
[2.5]: #custom-events
[3]: #example-usage-of-events

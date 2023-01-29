---
title: Client Events 
description: How to use Events correctly.
id: events
---

## Using Events 

### Table of Content
  - **[Understanding Events][1]**
  - **[Types of Events][2]**
     - **[Server based events][2.1]**
     - **[User based events][2.2]**
     - **[Client based events][2.3]**
     - **[Command & message based events][2.4]**
  - **[Example Usage][3]**
---

**aoi.js** has various event listeners, known as "events", that cater to the majority of events provided by the Discord API.

Each of them has its own usage and command type for executing specific tasks (for example, for logging purposes).

The events are not mandatory, apart from **`onMessage`** (which is required for the bot to read and send messages), but if you wish to utilise them, they must be included in your main file, in order for the bot to listen for those events. This is necessary in order to make use of the different command types.

It's worth bearing in mind that in order to utilise certain events, you'll need to activate your intents on the Discord Developer Portal.

## Types of Events

### Server based events:
* **onLeave** => for logging members once they leave servers
* **onJoin** => for logging members once they join servers
* **onBanAdd** => for logging members once they get banned in servers
* **onBanRemove** => for logging members once they get unbanned in servers
* **onChannelCreate** => for logging channels once they get created
* **onChannelDelete** => for logging channels once they get deleted
* **onChannelUpdate** => for logging channels once they get updated
* **onThreadCreate** => for logging threads once they get created
* **onThreadDelete** => for logging threads once they get deleted
* **onThreadUpdate** => for logging threads once they get updated
* **onRoleCreate** => for logging roles once they get created
* **onRoleDelete** => for logging roles once they get deleted
* **onRoleUpdate** => for logging roles once they get updated
* **onStageInstanceCreate** => for logging stage instance creations
* **onStageInstanceUpdate** => for logging stage instance updates
* **onStageInstanceDelete** => for logging stage instance deletions
* **onWebhookUpdate** => for logging webhook updates

### User based events:
* **onUserUpdate** => for logging users updating their profile
* **onMemberUpdate** => for logging members updates in a server
* **onPresenceUpdate** => for logging presence updates of users
* **onVoiceStateUpdate** => for logging voice state updates of members in a server

### Client based events:
* **onRateLimit** => for logging rate limits of the bot
* **onGuildJoin** => for logging what servers the bot joins
* **onGuildLeave** => for logging what servers the bot leaves

### Command & message based events:
* **onMessage** => for logging & responding to messages
* **onMessageDelete** => for logging messages which get deleted
* **onMessageUpdate** => for logging messages they get updated
* **onInteractionCreate** => for using slash commands
* **onReactionAdd** => for logging reactions on messages
* **onReactionRemove** => for logging removed reactions on messages

## Example Usage of Events

```js
const aoijs = require("aoi.js");

const bot = new aoijs.Bot({
  token: "DISCORD BOT TOKEN",
  prefix: "DISCORD BOT PREFIX",
  intents: ["Guilds", "GuildMessages", "MessageContent"],
  events: ["onMessage", "onJoin", "onLeave", "onBanAdd", "onBanRemove"]
});
```


<!--- links -->
[1]: #table-of-content
[2]: #types-of-events
[2.1]: #server-based-events
[2.2]: #user-based-events
[2.3]: #client-based-events
[2.4]: #command--message-based-events
[3]: #example-usage-of-events
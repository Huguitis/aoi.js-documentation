---
title: Using Events 
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
     - **[Using Events in your main file][3.1]**
---

**aoi.js** has various event listeners, known as "events", that cater to the majority of events provided by the Discord API.

Each of them has its own usage and command type for executing specific tasks (for example, for logging purposes).

The events are not mandatory, apart from **`bot.onMessage()`** (which is require for the bot to read and send messages), but if you wish to utilise them, they must be included in your primary file, in order for the bot to listen for those events. This is necessary in order to make use of the different command types.

It's worth bearing in mind that in order to utilise certain events, you'll need to activate your intents on the Discord Developer Portal.

## Types of Events

### Server based events:
* **bot.onLeave()** => for logging members once they leave servers
* **bot.onJoined()** => for logging members once they join servers
* **bot.onBanAdd()** => for logging members once they get banned in servers
* **bot.onBanRemove()** => for logging members once they get unbanned inservers
* **bot.onChannelCreate()** => for logging channels once they get created
* **bot.onChannelDelete()** => for logging channels once they get deleted
* **bot.onChannelUpdate()** => for logging channels once they get updated
* **bot.onRoleCreate()** => for logging roles once they get created
* **bot.onRoleDelete()** => for logging roles once they get deleted
* **bot.onRoleUpdate()** => for logging roles once they get updated

### User based events:
* **bot.onUserUpdate()** => for logging users updating their profile
* **bot.onMemberUpdate()** => for logging members updates in a server
* **bot.onPresenceUpdate()** => for logging presence updates of users
* **bot.onVoiceStateUpdate()** => for logging voice state updates of members in a server

### Client based events:
* **bot.onRateLimit()** => for logging rate limits of the bot
* **bot.onGuildJoin()** => for logging what servers the bot joins
* **bot.onGuildLeave()** => for logging what servers the bot leaves

### Command & message based events:
* **bot.onMessage()** => for logging & responding to messages
* **bot.onMessageDelete()** => for logging messages they get deleted
* **bot.onMessageUpdate()** => for logging messages they get updated
* **bot.onInteractionCreate()** => for using slash commands
* **bot.onReactionAdd()** => for logging reactions on messages
* **bot.onReactionRemove()** => for logging removed reactions on messages

## Example Usage of Events

### Using Events in your main file

```js
const aoijs = require("aoi.js");

const bot = new aoijs.Bot({
  token: "DISCORD BOT TOKEN",
  prefix: "DISCORD BOT PREFIX",
  intents: ["Guilds", "GuildMessages"]
});
 
bot.onMessage(); // Mandatory, always use this event (only if you have the required intents)
bot.onJoined(); // Allows to log users who join servers
bot.onLeave(); // Allows to log users who leave servers
bot.onBanAdd(); // Allows to log users who get banned from servers
bot.onBanRemove(); // Allows to log users who get unbanned from servers
```


<!--- links -->
[1]: #table-of-content
[2]: #types-of-events
[2.1]: #server-based-events
[2.2]: #user-based-events
[2.3]: #client-based-events
[2.4]: #command--message-based-events
[3]: #example-usage-of-events
[3.1]: #using-events-in-your-main-file

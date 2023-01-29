---
title: Client Status 
description: Status - How to use bot statuses.
id: status
---

#### This guide will be covering statuses and client presences.

### Table of Content
  - **[Statuses][1]**
  - **[Client Presence][2]** 
    -  **[Mobile Presence](#client-presence)**

---

### Bot Status

#### This section will cover how to customize your bot's status.

First of all we have to add the following piece of code to our main file:
```js
bot.status({
  text: "Example Text!",
  type: "PLAYING",
  time: 12
});
```
This will display the text "Example Text!" as bot status, of course you can modify it.

If you want to have multiple statuses just add multiple `bot.status({...})`, simple do the following:
```js
bot.status({
  text: "Example Text!",
  type: "PLAYING",
  time: 12
});

bot.status({
  text: "Example Text!",
  type: "WATCHING",
  time: 20
});

bot.status({
  text: "Example Text!",
  type: "STEAMING",
  url: "URL"
});
```

There are various types of statuses:

> * **PLAYING**
> * **WATCHING**
> * **STREAMING** 
> * **LISTENING**
> * **COMPETING**

### Client Presence 

You can also set the bot's presence, by adding the `status` property, for example:
```js
bot.status({
  text: "Example Text!",
  type: "PLAYING",
  status: "dnd"
  time: 12
});
```

There are multiple types of presences:

> * **online**
> * **idle**
> * **dnd** 
> * **invisible**
> * **mobilePresence**  
  > To use the mobile presence you have to setup something in your main file:
>  ```js
> const aoijs = require("aoi.js");
> 
> const bot = new aoijs.Bot({
>   token: "DISCORD BOT TOKEN",
>   prefix: "DISCORD BOT PREFIX",
>   intents: ["Guilds", "GuildMessages", "MessageContent"],
>   events: ["onMessage"],
>   mobilePlatform: true
> });
> ```

<!--- links -->
[1]: #bot-status
[2]: #client-presence

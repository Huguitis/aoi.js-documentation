---
title: Introduction
description: Setting up aoi.music with ease.
id: aoimusic-introduction
---

### Table of Content

- **[Installation](#installation)**
- **[Setup](#example-usage)**
- **[Callbacks](#callbacks)**
    - **[Adding Callbacks](#adding-callbacks)**
    - **[List of Callbacks](#list-of-callbacks)**
    - **[Using Callbacks](#using-callbacks)**
- **[Soundcloud ID](#getting-your-soundcloud-id)**

---

### Installation

**node.js 16.9.0 or newer is required.**

```bash
npm install @akarui/aoi.music
```

```bash
# for Edge
npm install @akarui/aoi.music@dev
# or
npm install https://github.com/akaruidevelopment/music#main
```

### Options

```js
const voice = new AoiVoice(bot, {
    searchOptions?: {
        soundcloudClientId?: string,
        youtubeCookie?: string,
        youtubeAuth?: PathLike,
        youtubegl?: string,
        youtubeClient?: "WEB" | "ANDROID" | "YTMUSIC",
    },
    requestOptions?: {
        offsetTimeout?: number,
        soundcloudLikeTrackLimit?: number,
        youtubePlaylistLimit?: number,
        spotifyPlaylistLimit?: number,
    },
    devOptions?: {
        debug: boolean,
    },
});
```

### Example Usage

```javascript
const { AoiClient } = require("aoi.js");
const { AoiVoice, PlayerEvents, PluginName, Cacher, Filter } = require("@akarui/aoi.music");

const bot = new AoiClient({
    token: "Discord Bot Token",
    prefix: "Discord Bot Prefix",
    intents: ["MessageContent", "Guilds", "GuildMessages", "GuildVoiceStates"],
    events: ["onMessage", "onInteractionCreate"],
    database: {
        type: "aoi.db",
        db: require("aoi.db"),
        tables: ["main"],
        path: "./database/",
        extraOptions: {
            dbType: "KeyValue"
        }
    }
});

const voice = new AoiVoice(bot, {
    searchOptions: {
        soundcloudClientId: "Soundcloud ID",
        youtubegl: "US",
    },
    requestOptions: {
        offsetTimeout: 0,
        soundcloudLikeTrackLimit: 200,
    },
});

// Command Example (ping)
bot.command({
    name: "ping",
    code: `Pong! $pingms`,
});

// optional (cacher / filter)
voice.addPlugin(PluginName.Cacher, new Cacher("memory" /* or "disk" */));
voice.addPlugin(PluginName.Filter, new Filter({
    filterFromStart: false,
}));
```

### Callbacks

#### Adding Callbacks

```js
voice.addEvent("eventName");
```

#### List of Callbacks

- `trackStart` &rarr; Emitted whenever a track starts. 
- `trackEnd` &rarr; Emitted whenever a track ends.
- `queueStart` &rarr; Emitted whenever a queue starts.
- `queueEnd` &rarr; Emitted whenever a queue ends.
- `audioError` &rarr; Emitted whenever a audio error occurs.
- `trackPause` &rarr; Emitted whenever a track pauses.
- `trackResume` &rarr; Emitted whenever a track resumes.

### Using Callbacks

```js
loader.load(voice.cmds,"./voice/") // loader being the LoadCommands class
```

This should be the content of your `/voice/somefile.js`:

```js
module.exports = [{
    channel: "$channelID",
    type: "eventName",
    code: `code to execute here`
}]
```

If you don't want to use handlers, you can use this instead in your main file:

```js
voice.cmds["eventName"].set("name of the command", {
    channel: "$channelID",
    code: `code to execute here`
});
```

### Getting your SoundCloud ID

Head to the [SoundCloud](https://soundcloud.com/) website and make sure you're logged in.

1. Press <kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>I</kbd> or <kbd>F12</kbd>

2. Head to the `Network` tab and refresh the page if necessary.

3. Play a random song and search for a property with `?clientID=`.

4. Copy the characters after that and you're done.

![preview](https://cdn.discordapp.com/attachments/1082168708866244648/1089057487690399856/wNZ1ZwP2xFAEAAAAABJRU5ErkJggg.png)
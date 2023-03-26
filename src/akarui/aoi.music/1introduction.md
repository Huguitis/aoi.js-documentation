---
title: Introduction
description: Setting up aoi.music with ease.
id: aoimusic-introduction
---

### Table of Content

- **[Installation](#installation)**
- **[Setup](#example-usage)**

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
const { AoiVoice } = require("@akarui/aoi.music");

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

// Command Example (ping)
bot.command({
    name: "ping",
    code: `Pong! $pingms`,
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
```

### Getting your SoundCloud ID

Head to the [SoundCloud](https://soundcloud.com/) website and make sure you're logged in.

1. Press <kbd>CTRL</kbd> / <kbd>⌘</kbd> + <kbd>SHIFT</kbd> + <kbd>I</kbd> or <kbd>F12</kbd>

2. Head to the `Network` tab and refresh the page if necessary.

3. Play a random song and search for a property with `?clientID=`.

4. Copy the characters after that and you're done.

![preview](https://cdn.discordapp.com/attachments/1082168708866244648/1089057487690399856/wNZ1ZwP2xFAEAAAAABJRU5ErkJggg.png)
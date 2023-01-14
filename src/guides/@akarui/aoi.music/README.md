---
title: akarui/aoi.music
description: How to integrate aoi.music into your Discord Bot with ease.
id: akarui/aoi.music
---

# @akarui/aoi.music Documentation

## Table Of Contents

| Name | Description | Link |
| -------- | -------- | -------- |
| Options | Dev, Search & Request Options | [link](/src/guides/@akarui/aoi.music/options.md) | 
| Functions | All aoi.js extension functions | [link](/src/guides/@akarui/aoi.music/funcs.md) | 



## Installation

### node.js 16.9.0 or newer is required.

```bash
npm install @akarui/aoi.music
```

## Example Usage:
```javascript
const aoijs = require("aoi.js");
const { AoiVoice } = require("@akarui/aoi.music");

const bot = new aoijs.AoiClient({
    token: "Discord Bot Token",
    prefix: "Discord Bot Prefix",
    intents: ["MessageContent", "Guilds", "GuildMessages", "GuildVoiceStates"],
});

//Events
bot.onMessage();

//Command Example (ping)
bot.command({
    name: "ping",
    code: `Pong! $pingms`,
});

const voice = new AoiVoice(bot, {
    searchOptions: {
        soundcloudClientId: "Sound Cloud Id",
        youtubegl: "US",
    },
    requestOptions: {
        offsetTimeout: 0,
        soundcloudLikeTrackLimit: 200,
    },
});
```



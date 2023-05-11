---
title: Introduction
description: The basic introduction of @akarui/aoi.music
---

aoi.js has an extension named ***@akarui/aoi.music*** for music.

## Notice

If you have issues such the Client not joining the Voice Channel, make sure you have the latest version of aoi.js and @akarui/aoi.music.

As well you have added `GUILD_VOICE_STATES` intent to your intents array.

```diff
- intents: ["GUILDS", "GUILD_MESSAGES"]
+ intents: ["GUILDS", "GUILD_MESSAGES", "GUILD_VOICE_STATES"]
```
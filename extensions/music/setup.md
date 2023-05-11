---
title: Setup
description: How to setup @akarui/aoi.music
---

To even begin using @akarui/aoi.music you will need to install it.

After installation is done, you can begin by following the **[Usage](#usage)** section.

## Installation

```bash
npm i @akarui/aoi.music
```

## Usage

```javascript title="index.js"
const { Voice, LoadCommands, Bot } = require("aoi.js");

const bot = new Bot({
  token: "DISCORD BOT TOKEN",
  prefix: "DISCORD BOT PREFIX",
  intents: ["GUILDS", "GUILD_MESSAGES", "GUILD_VOICE_STATES"]
});

const loader = new LoadCommands(bot);

const voice = new Voice(
  bot,
  {
    cache: {
      cacheType: "Memory",//Disk
      enabled: true,
      //directory : "music", only for Disk type
    },
  },
  false, //to enable pruneMusic 
);

voice.onTrackStart();

loader.load(bot.cmd, "./commands/"); //bot cmds
loader.load(voice.cmd, "./commands/voice/"); //voice cmds
```

## Usage + Soundcloud

```javascript title="index.js"
const { Voice, LoadCommands, Bot } = require("aoi.js");

const bot = new Bot({
  token: "DISCORD BOT TOKEN",
  prefix: "DISCORD BOT PREFIX",
  intents: ["GUILDS", "GUILD_MESSAGES", "GUILD_VOICE_STATES"]
});

const loader = new LoadCommands(bot);

const voice = new Voice(
  bot,
  {
    cache: {
      cacheType: "Memory",//Disk
      enabled: true,
      //directory : "music", only for Disk type
    },
    soundcloud: {
      clientId : "SOUNDCLOUD CLIENT ID",
      limitLikeTrack : 200 
    },//optional
  },
  false, //to enable pruneMusic 
);
```

### PlayerOptions

```javascript title="index.js"
  playerOptions: {
    trackInfoInterval: 5000,
  },//optional
```
### PruneMusic

Just update the `false` to `true` if you wish to enable prune music within the premade voice method.

```diff title="index.js"
- false,
+ true,
```

## Notice

If you have issues such the Client not joining the Voice Channel, make sure you have the latest version of aoi.js and @akarui/aoi.music.

As well you have added `GUILD_VOICE_STATES` intent to your intents array.

```diff
- intents: ["GUILDS", "GUILD_MESSAGES"]
+ intents: ["GUILDS", "GUILD_MESSAGES", "GUILD_VOICE_STATES"]
```

## Example

### Play

```javascript title="commands/voice/play.js"
module.exports = {
  name: "play",
  $if: "v4", //enabling pseudo $if
  code: `
    $let[msg;$playTrack[youtube;$message]]

    $if[$hasPlayer==false]
        $joinVc
    $endif

    $onlyif[($voiceId[$clientId]!=)&&($voiceId[$clientId]==$voiceId);you are not in the same voice channel]
    $onlyif[$voiceId!=;join a voice channel before using play cmd]
    `,
};
```

### Queue

```javascript title="commands/voice/queue.js"
module.exports = {
  name: "queue",
  code: `
   $title[1;Queue]
   $author[1;Requested By $usertag;$authorAvatar]
   $description[1;$queue[$if[$message==;1;$message]]]
   $footer[1;number of songs ->$queueLength]
   $color[1;RANDOM]
   $addTimestamp[1]
    `,
};
```

### onTrackStart event

```javascript title="commands/voice/onTrackStart.js"
module.exports = {
  name: "newTrack", //optional
  type : "trackStart",
  channel : "$channelID",
  code: `
	  $title[1;Now Playing...]
	  $description[1;$if[$musicEventData[info.description]==;description not available;$musicEventData[info.description]]]
      $color[1;RANDOM]
	  $author[1;$musicEventData[info.title]]
	  $image[1;$musicEventData[info.thumbnail]]
    `,
};
```
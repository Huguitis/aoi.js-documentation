<p align="center">
  <a href="https://aoi.js.org">
    <img width="650" src="https://camo.githubusercontent.com/aaf8a38df828f097ecddcd3e4e72441a5d9a66d032e2a7a0b42f68c2ad708c79/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f313035383834333432383833313632393434332f313036333235313737303232383334323839352f616f696a7362616e6e65722e706e67" alt="aoijs">
  </a>
</p>

<h1 align="center">aoi.js documentation</h1>

<div align="center">

**The official Documentation of the aoi.js NPM package.**
  
[![NPM downloads][download-image]][download-url]
[![AoiJS Server][aoijs-server]][aoijs-server-url]
[![NPM version][npm-image]][npm-url]

[npm-image]: http://img.shields.io/npm/v/aoi.js.svg?color=42cfff
[npm-url]: http://npmjs.org/package/aoi.js
[download-image]: https://img.shields.io/npm/dt/aoi.js.svg?color=3182b0
[download-url]: https://npmjs.org/package/aoi.js
[aoijs-server]: https://img.shields.io/discord/773352845738115102?color=5865F2&logo=discord&logoColor=white
[aoijs-server-url]: https://aoi.js.org/invite

</div>

## Features

- Built-in support of [database](https://www.npmjs.com/package/aoi.db) by default and ready for multipurpose.
- Built-in 600+ functions, simple and easy to learn.
- Simple to learn, all in string-based and compact.
- Support of extensions available to be used by the community.

## Installation

**node.js 16.9.0 or newer is required.**

```bash
npm install aoi.js
yarn add aoi.js
```

## Setup

```javascript
const aoijs = require("aoi.js")
const bot = new aoijs.AoiClient({
token: "Discord Bot Token",
prefix: "Discord Bot Prefix",
intents: ["MessageContent", "Guilds", "GuildMessages"]
});

//Events
bot.onMessage();

//Command Example (ping)
bot.command({
name: "ping",
code: `Pong! $pingms`
});
```
    
## Disclaimer
    
Aoi.js is not affiliated or associated with Discord or any other services.
    
## Links
- [Website](https://aoi.js.org)
- [NPM](https://www.npmjs.com/package/aoi.js)
- [Github](https://github.com/AkaruiDevelopment/aoi.js)
- [Discord Support Server](https://discord.gg/HMUfMXDQsV)
- [Documentation](https://aoi.js.org/docs/)

---
title: aoi.panel
description: Setting up aoi.panel with ease.
id: aoi.panel
---

# @akarui/aoi.panel Documentation

## Table Of Contents

| Name | Description | Link |
| -------- | -------- | -------- |
| The panel Class | The panel Class and its parameters | [link](/src/guides/@akarui/aoi.panel/panel.md) | 
| Functions | loadPanel and onError | [link](/src/guides/@akarui/aoi.panel/funcs.md) | 
| Advanced Features | Multiple accounts, custom pages, etc. | [link](/src/guides/@akarui/aoi.panel/advanced.md) | 

## To View Examples Click [here](https://github.com/AkaruiDevelopment/panel/blob/main/examples/)


## Installation

```bash
npm i @akarui/aoi.panel
```

## Basic Usage (aoi.js v5):
```javascript
const {Panel} = require("@akarui/aoi.panel")

const {AoiClient} = require("aoi.js")


const bot = new AoiClient({
  token: "Discord Bot Token",
  prefix: "Discord Bot Prefix",
  intents: ["MessageContent", "Guilds", "GuildMessages"],
  events: ["onMessage"]
});

const panel = new Panel({
    username: "your-username",//username for logging in
    password: "password-here",//password for logging in
    secret: require('crypto').randomBytes(16).toString("hex"),//session secret
    port: 3000,//port on which website is hosted, Not required! Default 3000
    bot: bot,//your aoi.js client
    mainFile: "index.js",//Main file where code is running.Not required, default taken from package.json
    commands: "./commands",// folder name in which all the edit needing files are there.
    interaction:"./interactions"//interactions folder
})
panel.loadPanel()//Load The Panel

panel.onError()//Will detect errors, and send it to aoi.panel's error page.

```
LOGIN PAGE
![image](https://user-images.githubusercontent.com/85351846/203999818-50ff6898-fdee-49c8-8ade-0f94df4c0248.png)

MAIN PANEL PAGE
![image](https://user-images.githubusercontent.com/85351846/204000002-d2de03e3-d4cd-4791-80b3-afbbc8225863.png)

GUILDS PAGE
![image](https://user-images.githubusercontent.com/85351846/204000224-d1ff27f2-ed6d-4da4-8f93-27ece09d09a4.png)


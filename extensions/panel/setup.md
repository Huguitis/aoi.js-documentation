---
title: Setup
description: How to setup @akarui/aoi.panel
---

To even begin using @akarui/aoi.panel you will need to install it.

After installation is done, you can begin by following the **[Usage](#usage)** section.

## Installation

```bash
npm install @akarui/aoi.panel
```

## Usage

```javascript title="index.js"
const {Panel} = require("@akarui/aoi.panel")

const panel = new Panel({
    username: "your-username",//username for logging in
    password: "password-here",//password for logging in
    secret: "aoijs",//session secret
    port: 3000,//port on which website is hosted, Not required! Default 3000
    bot: bot,//your aoi.js client
    mainFile: "index.js",//Main file where code is running.Not required, default taken from package.json
    commands: "commands"// folder name in which all the edit needing files are there
})
panel.loadPanel()//Load The Panel

panel.onError()//Will detect errors, and send it to aoi.panel's error page
```

This should be inside of your **main file**, which is likely named as `index.js` or something similar.

## Methods

- **username**: Username for logging in.
- **password**: Password for logging in.
- **secret**: Session secret.
- **port**: Port on which website is hosted.
- **bot**: Your aoi.js client.
- **mainFile**: Main file where code is running.
- **commands**: Folder name in which all the edit needing files are there.
- **onError**: Will detect errors, and send it to aoi.panel's error page. (event)
- **loadPanel**: Load The Panel.
- **onError**: Will detect errors, and send it to aoi.panel's error page. (event)
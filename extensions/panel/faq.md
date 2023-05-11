---
title: FAQ
description: Know more about @akarui/aoi.panel and how to use it.
---

## Known Errors

### `ENOTDIR: not a directory, rename 'document.getElementByID(name).value' -> '/home/runner/aoi.panel/commands/'`

You didn't give a name to the file when creating a command.
> Latest update now pops up a message box to force a file name.

### `Oops, looks like the bot has not yet been initialized. Try again in a few minutes.`

Your Aoi client has not yet started. 
If using Replit, type `kill 1` in the shell and the run your code.

Make sure you have the latest version of aoi.js as well sufficient resources available. 

### `Cannot find module <some package name> Require stack: /home/runner/aoi.panel/`

Missing dependencies in your package.json. Install them and try again.

### `Uncaught Exception/Catch Error: ENOENT: no such file or directory, open '/home/runner/aoi.panel/node_modules/@akarui/aoi.panel/src/errors/<random string was here>.txt'`

An older version of panel did not have the proper error directory, update to the latest by `npm i @akarui/aoi.panel@latest`
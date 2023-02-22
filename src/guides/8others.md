---
title: Others
description: This guide is covering, client options, databases, command aliases and hyperlinks.
id: others
---

#### This guide will be covering every question you may have.

### Table of Content

- **[Client Options](#client-options)**
- **[Database](#databases)**
    - **[aoi.db](#aoidb)**
- **[Command Aliases][1]**
    - **[Way more possibilities][1.1]**
- **[Hyperlinks][2]**
    - **[Tool Tips](#hovering-text)**

---

## Client Options

```typescript
const aoijs = require("aoi.js");

const bot = new aoijs.AoiClient({
    token: string,
    prefix: string,
    intents: ["MessageContent", "Guilds", "GuildMessages"],
    events: ["onMessage", "onJoin", "onLeave"],
    disableFunctions: ["$function", "$function"],
    plugins: ["./path"],
    respondToBots: boolean,
    guildOnly: boolean,
    autoUpdate: boolean,
    mobilePlatform: boolean,
    cache: {
        users: number,
        messages: number,
    },
    database: {
        type: "aoi.db",
        db: require("aoi.db"),
        tables: ["main"],
        path: "./database/",
        extraOptions: {
            dbType: "KeyValue",
        }
    }, // Example refers to aoi.db, other databases are not included in this Example.
    suppressAllErrors: boolean,
    errorMessage: string,
    aoiWarning: boolean,
    aoiLogs: boolean,
    respondOnEdit: {
        commands: boolean,
        alwaysExecute: boolean,
        nonPrefixed: boolean,
        time: number
    },
});
```

### Databases

#### aoi.db

Install **aoi.db**:

```typescript
npm
i
aoi.db
```

Usage of aoi.db in your main file:

```js
const aoijs = require("aoi.js");

const bot = new aoijs.AoiClient({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["Guilds", "GuildMessages", "MessageContent"],
    events: ["onMessage"],
    database: {
        type: "aoi.db",
        db: require("aoi.db"),
        tables: ["main"],
        path: "./database/",
        extraOptions: {
            dbType: "KeyValue",
        }
    });
```

In case this doesn't work, make sure you have a directory called "database", inside it a directory called "main" and a
file called "main_scheme_1.sql" with the content of "{}".

## Command Aliases

#### Command aliases work just like command names, but they will also trigger the same command!

```js
aliases: ["alias1", "alias2"],
```

Simply add that under `name: "..."` and you're ready to go!

```js
bot.command({
    name: "say",
    aliases: ["repeat"],
    code: `
  You said: "$message"!
  `
});
```

```js
module.exports = [{
    name: "say",
    aliases: ["repeat"],
    code: `
  You said: "$message"!
  `
}];
```

### Way more possibilities

#### You could add even more than just aliases to your command, things like descriptions, categories.. everything is possible.

```js
bot.command({
    name: "say",
    aliases: ["repeat"],
    category: "misc",
    usage: "[prefix]say <message>",
    code: `
  You said: "$message"!
  `
});
```

```js
module.exports = [{
    name: "say",
    aliases: ["repeat"],
    category: "misc",
    usage: "[prefix]say <message>",
    code: `
  You said: "$message"!
  `
}];
```

```js
module.exports = [{
    name: "say",
    aliases: ["repeat"],
    info: {
        name: "say",
        category: "misc",
        usage: "[prefix]say <message>"
    },
    code: `
  You said: "$message"!
  `
}];
```

And the great thing is you can get that information using `$commandInfo`!

```php
$commandInfo[commandName;property]

$commandInfo[commandName;property.sub]
```

## Hyperlinks

#### Hyperlinks are pretty useful to link other websites in embeds or interactions.

Please note that this only works in embeds and interactions. Meaning it won't work in regular messages.

#### Examples

Lets say we want to embed the https://aoi.js.org link in our embed, first of all we have to look at the formatting:

```js
[aoi.js is great!](https
://aoi.js.org)
```

That will make sure that out link is embedded in "aoi.js is great!". As next we add the embed:

```js
$description[Want
to
learn
more
about
aoi.js ? Click [here](https ://aoi.js.org)!]
```

This will embed the link in the word "here" and redirect you to the website when you click the word.

#### Hovering Text

Want to have hovering text when hovering over the word? Simple!

```js
[aoi.js is great!](https
://aoi.js.org "not everyone sees this" )
```

This will add the label "not everyone sees this" when you hover over the text for a while.

```js
$description[Want
to
learn
more
about
aoi.js ? Click [here](https ://aoi.js.org "aoi.js is great")!]
```

<!--- links -->

[1]: #command-aliases

[1.1]: #way-more-possibilities

[2]: #hyperlinks

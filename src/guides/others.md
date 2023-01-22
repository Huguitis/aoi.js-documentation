---
title: others 
description: others - aliases and hyperlinks
id: others
---

## Parsers

#### This guide will be covering every question you may have.

### Table of Content
  - **[Command Aliases][1]**
    - **[Way more possibilities][1.1]**  
  - **[Hyperlinks][2]**

---

### Command Aliases

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

---

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

---

### Hyperlinks

#### Hyperlinks are pretty useful to link other websites in embeds or interactions.

Please note that this only works in embeds and interactions. Meaning it won't work in regular messages.

#### Examples

Lets say we want to embed the https://aoi.js.org link in our embed, first of all we have to look at the formatting:
```js
[aoi.js is great!](https://aoi.js.org)
```
That will make sure that out link is embedded in "aoi.js is great!". As next we add the embed:
```js
$description[Want to learn more about aoi.js? Click [here](https://aoi.js.org)!]
```
This will embed the link in the word "here" and redirect you to the website when you click the word.

#### Hovering Text

Want to have hovering text when hovering over the word? Simple!

```js
[aoi.js is great!](https://aoi.js.org "not everyone sees this" )
```

This will add the label "not everyone sees this" when you hover over the text for a while.

```js
$description[Want to learn more about aoi.js? Click [here](https://aoi.js.org "aoi.js is great")!]
```


<!--- links -->
[1]: #command-aliases
[1.1]: #way-more-possibilities
[2]: #hyperlinks

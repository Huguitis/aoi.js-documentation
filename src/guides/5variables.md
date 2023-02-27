---
title: Variables
description: This Guide will be covering variables, their usag and how to store variables in other files.
id: variables
---

#### This guide will be covering everything you need to know about variables.

### Table of Content

- **[Using Variables][1]**
- **[Variable Handler][2]**

---

### Using Variables

#### Variables are very helpful, and makes devolping a lot easier.

Before we use variables, we have to learn how to use them.

```js
bot.variables({
    varname: "varvalue",
    varname2: "varvalue2"
});
```

This is the easiest out of two ways to use variables.

### Variable Handler

#### Another way, which will keep your main file clean, are variable handlers.

Create a directory called "**handler**" and a file inside of it called "**variables.js**", after you did that, put that
in your main file:

```js
bot.variables(require("./handler/variables.js"));
```

Now go to your `variables.js` file and paste the following:

```js
module.exports = {
    varname: "varvalue",
    varname2: "varvalue2"
}
```

And that's it, you have a working variable handler!

<!--- links -->

[1]: #using-variables

[2]: #variable-handler

[3]: #variable-functions

[embed-example]: https://cdn.discordapp.com/attachments/1061712111052521493/1061764337691279460/image_3.png

[aoi-github]: https://github.com/akaruidevelopment/aoi.js#v6

[ayaka-parser]: https://github.com/usersatoshi/parsers#main

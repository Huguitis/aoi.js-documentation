---
title: Parser 
description: Embed parser - How to use it.
id: parser
---

## Embed Parser

#### This guide will be covering everything you need to know about parsers.

### Table of Content
  - **[Embed Parser][1]**
    - **[Basics][1]**
    - **[Examples][1]**

---

### Embed Parser
#### Embed Parser are quite easy to use once you know how, this section will be covering the basics about embed parsers and some examples for you to work with.

To use embed parsers we have to understand the basics first.

If you want to send embeds using `$sendMessage` or `$channelSendMessage` then you must use `{newEmbed:}` before creating an embed. Lets say we want our title to be "This is an great example of using embed parsers!". 

So we use `{title:}` for our title and put that in `{newEmbed:}`. It should look like the following:

```js
{newEmbed:{title:This is an great example of using embed parsers!}}
``` 

The embed looks quite sad with just a title, lets add some color and a simple description.

```js
{newEmbed:{title:This is an great example of using embed parsers!}{description:I love the color Red!}{color:Red}}
``` 

You want to add an image? No problem, simply use `{image:url}` but make sure to escape the colons ( `:` ) in the URL or else it might break the parser completely and we don't want that for sure. We can do that with either `#COLON#` or with a backslash ( `\` ).

```js
{newEmbed:{title:This is an great example of using embed parsers!}{description:I love the color Red!}{image:https\://cdn.discordapp.com/icons/773352845738115102/f6b0d1a62a83397976ea441c5377e6ad.png?size=128}{color:Red}}
``` 

Our final code should look like this:

```js
$sendMessage[{newEmbed:{title:This is an great example of using embed parsers!}{description:I love the color Red!}{image:https\://cdn.discordapp.com/icons/773352845738115102/f6b0d1a62a83397976ea441c5377e6ad.png?size=128}{color:Red}}]
```

Your result looks like this if you did everything correct:

![embed-example][embed-example]

### Embed Parsers Examples

##### Embed with title, description, footer, author / author icon  and color.

```js
{newEmbed:{author:Aoi.js is great:https\://cdn.discordapp.com/icons/773352845738115102/f6b0d1a62a83397976ea441c5377e6ad.png?size=128}{title:Awesome Example!}{description:I love embed parsers!}{footer:Example #1}{color:Blue}}
```

##### Embed with title, footer, image and field.

```js 
{newEmbed:{title:Another Awesome Example!}{image:https\://cdn.discordapp.com/icons/773352845738115102/f6b0d1a62a83397976ea441c5377e6ad.png?size=128}{field:This is a field title!:And a field description which is not inline!:no}{footer:Example #2}}
``` 


<!--- links -->
[1]: #embed-parsers
[2]: #parsers
[2.1]: #installing-packages
[2.2]: #basic-parser-examples
[2.3]: #parser-examples
[embed-example]: https://cdn.discordapp.com/attachments/1061712111052521493/1061764337691279460/image_3.png
[aoi-github]: https://github.com/akaruidevelopment/aoi.js#v6
[ayaka-parser]: https://github.com/usersatoshi/parsers#main

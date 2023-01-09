---
title: Parser 
description: Embed parser - How to use it.
id: parser
---

## Parsers

#### This guide will be covering everything you need to know about parsers.

### Table of Content
  - **[Embed Parsers][1]**
    - **[Basics][1]**
    - **[Examples][1]**
  - **[JSON Parsers][2]**
    - **[Installing Packages][2.1]**
    - **[Basics][2.2]**
    - **[Examples][2.3]**

#### **JSON Parsers currently only work in the github version ([aoi.js@6.0.3][aoi-github])**

---

### Embed Parsers
#### Embed Parsers are quite easy to use once you know how, this section will be covering the basics about embed parsers and some examples for you to work with.

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

---

### Parsers
#### **Parsers currently only work in the github version ([aoi.js@6.0.3][aoi-github])**

### Installing Packages

You have to install a package to use parsers. Unfortunately they decided to remove JSON parsers.

**aoi.js** github version: <br>
`npm i https://github.com/akaruidevelopment/aoi.js#v6`

**aoi.js** parsers: <br>
`npm i https://github.com/usersatoshi/parsers#main`

After you installed both, add this to the top of your main file.
```js
const { Util } = require("aoi.js");
const { parse } = require("aoi.parser");
Util.parsers.ErrorHandler = parse;
```

You're now able to use parsers.

### Basic Parser Examples

#### This is mainly used to add Message Components such as buttons, select menus and text inputs. This guide will *only* cover buttons.

Lets start with the structure, you need `{actionRow:}`, no matter what you do. Inside of it are going to be our components later on.

```js
{button:Button Label:Type:Custom ID:disabled}
```

```js
{button:Example Button!:1:exampleButton:no}
```
<details>
  <summary> <h3> Button Types </h3></summary>

| Name      | ID  |  Color  |
| --------- | :-: | :-----: |
| Primary   |	1 	| blurple |	
| Secondary |	2	  | grey    |	
| Success   |	3   |	green   |	
| Danger    |	4   |	red     |
| Link	    | 5  	| grey    |

  ### Make sure to use the ID as button style.

</details>

### Parser Examples

```js
{actionRow:{actionRow:{button:Example Button!:1:exampleButton1:no}} //adds one button
```
```js
{actionRow:{actionRow:{button:Example Button!:1:exampleButton1:no}{button:Example Button!:2:exampleButton2:no}} //adds two buttons in the same row
```
```js
{actionRow:{actionRow:{button:Example Button!:1:exampleButton1:no}}{actionRow:{button:Example Button!:2:exampleButton2:no}} //adds two buttons in two different rows
```

Add all buttons for example: (make sure to escape the colon, stated in the embed parser guide)
```js
{actionRow:{button:Example Button!:1:exampleButton1:no}{button:Example Button!:2:exampleButton2:no}{button:Example Button!:4:exampleButton3:no}{button:Example Button!:3:exampleButton4:no}{button:Example Button!:5:https://discord.com:no}}{actionRow:{button:Example Button!:1:exampleButton1.1:yes}{button:Example Button!:2:exampleButton2.1:yes}{button:Example Button!:4:exampleButton3.1:yes}{button:Example Button!:3:exampleButton4.1:yes}{button:Example Button!:5:https://discord.com:yes}}
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

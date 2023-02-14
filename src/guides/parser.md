---
title: Parser 
description: Parser - embed parsers, component parsers, including basics and examples.
id: parser
---

#### This guide covers everything you need to know about embed parsers, component parsers, including basics and examples.

### Table of Content
  - **[Embed Parser](#embed-parser)**
    - **[Embeds](#embed-parser-functions)**
  - **[Components Parser](#components-parser)**
    - **[Button Parser](#button-parser)**
    - **[Select Menu Parser](#select-menu-parser)**
    - **[Interaction Modal Parser](#interaction-modal-parser)**
  - **[Examples](#parsers-examples)**
    - **[Embed Parser Examples](#embed-parser-1)**
    - **[Component Parser Examples](#components-parser-1)**
    - **[Interaction Modal Parser Example](#interaction-modal-parser-1)**

---

## Embed Parser
Embed Parser are quite easy to use once you know how, this section will be covering the basics about embed parsers. You require `{newEmbed:{...}}` every time you want to use embed parsers.

### Embed Parser Functions

```ts
{title:text}
{description:text}
{color:...}
{footer:text:icon?}
{image:url}
{thumbnail:url}
{author:name:icon?}
{authorURL:url}
{field:title:value:inline? (true/false)}
{timestamp:ms?}
``` 

---

## Components Parser

For every component parser is one thing always the same, `{actionRow:{...}}`. We use that to declare the arguments inside of it as components.  

### Button Parser

Usage:
```ts
{button:label:style:customID:disabled? (true/false):emoji?}
```

<details open>
  <summary><h3> Button Types </h3></summary>

| Name      | Value | Color                     |                                                                     |
|-----------|-------|---------------------------|---------------------------------------------------------------------|
| Primary   | 1     | blurple                   | `{button:Example Button!:primary:customID:false}`                   |
| Secondary | 2     | grey                      | `{button:Example Button!:secondary:customID:false}`                 |
| Success   | 3     | green                     | `{button:Example Button!:success:customID:false}`                   |
| Danger    | 4     | red                       | `{button:Example Button!:danger:customID:false}`                    |
| Link      | 5     | grey, navigates to a URL  | `{button:Example Button!:link:https\\:discord.gg:false}`            |
| Emoji     | 0     | primary button with emoji | `{button:Example Button!:primary:customID:false:emojiName,emojiID}` |

</details>

### Select Menu Parser

Usage:
```js
{selectMenu:customID:placeholder:minValue:maxValue:default (true/false):...options}

{selectMenuOptions:optionName:customID:optionDescription:default? (true/false):emoji?}
```

### Interaction Modal Parser

Usage:
```js
{textInput:label:style:customID:required? (true/false):placeholder?:minLength?:maxLength?:defaultValue?}
```


## Parsers Examples

### Embed Parser

**Embed with title, description, footer, author / author icon  and color.**

```js
{newEmbed:{author:Aoi.js is great:https\\://cdn.discordapp.com/icons/773352845738115102/f6b0d1a62a83397976ea441c5377e6ad.png?size=128}{title:Awesome Example!}{description:I love embed parsers!}{footer:Example #1}{color:Blue}}
```

**Embed with title, footer, image and field.**

```js 
{newEmbed:{title:Another Awesome Example!}{image:https\\://cdn.discordapp.com/icons/773352845738115102/f6b0d1a62a83397976ea441c5377e6ad.png?size=128}{field:This is a field title!:And a field description which is not inline!:false}{footer:Example #2}}
```

---

### Components Parser

#### Button Parser

**Two buttons each one in a different row.**

```js
{actionRow:{button:Button:secondary:button1}}{actionRow:{button:Button:primary:button2}}
```

**Three buttons one disabled and one with emoji.**

```js
{actionRow:{button:Button:primary:button1:true}{button:Button:primary:button2}{button:Button:danger:button3:false:👋}}
```

#### Select Menu Parser

**Single-Select Menu with two options**

```js
{actionRow:{selectMenu:customID:Placeholder:1:1:false:{selectMenuOptions:Option 1:1:Option Description 1:false:👋}{selectMenuOptions:Option 2:2:Option Description 2:false}}}
```

**Multi-Select Menu with three options and and a maximum of 2 selectable options**

```js
{actionRow:{selectMenu:customID:Placeholder:1:2:false:{selectMenuOptions:Option 1:1:Option Description 1:false:👋}{selectMenuOptions:Option 2:2:Option Description 2:false}{selectMenuOptions:Option 3:3:Option Description 3:false}}}
```

#### Interaction Modal Parser

**Modal with two fields one being normal sized and the other being bigger.**

```js
{actionRow:{textInput:Example Title 1:1:customID1:true}}{actionRow:{textInput:Example Title 2:2:customID2:false}}
```


<!--- links -->
[1]: #embed-parsers
[embed-example]: https://cdn.discordapp.com/attachments/1061712111052521493/1061764337691279460/image_3.png
[aoi-github]: https://github.com/akaruidevelopment/aoi.js#v6
[ayaka-parser]: https://github.com/usersatoshi/parsers#main

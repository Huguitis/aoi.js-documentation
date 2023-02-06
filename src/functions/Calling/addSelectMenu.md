---
title: $addSelectMenu 
description: $addSelectMenu will add a select menu to the bot's message.
id: addSelectMenu
---

`$addSelectMenu` will add a select menu to the bot's message.

## Usage

```php
$addSelectMenu[index;customId;placeHolder;minValues;maxValues;disabled?;label:description:value:default?:emoji?;...]
```

## Parameters 


| Field       | Type    | Description                                                | Required |
| ----------- | ------- | ---------------------------------------------------------- |:--------:|
| index       | integer | in which row the button appears                            |    yes   |
| customID    | string  | button custom ID                                           |    yes   |
| placeHolder | string  | select menu placeholder text                               |    yes   |
| minValues   | integer | select menu min value                                      |    yes   |
| maxValues   | integer | select menu max value                                      |    yes   |
| disabled    | string  | disabled? <br /> 1. **true** <br /> 2. **false** (default) |    yes   |
| options     | string  | options                                                    |    yes   |



## Example(s)

This adds a primary and link button to the bot's message:

```javascript
bot.command({
  name: "add-select-menu",
  code:`
  Select an option.
  
  $addSelectMenu[1;yourCustomID;This is a placeholder!;1;1;false;A Option:Description of option B:anotherCustomID:false;B Option:Description of option B:andAnotherCustomID:true]
  `
});

bot.interactionCommand({
  name: "yourCustomID",
  prototype: "selectMenu", 
  code: `
  $interactionReply[Hello! :);;;;everyone;false]
  $onlyIf[$interactionData[values[0]]==anotherCustomID;]
  `
});

bot.interactionCommand({
  name: "yourCustomID",
  prototype: "selectMenu", 
  code: `
  $interactionReply[Hello! :);;;;everyone;false]
  $onlyIf[$interactionData[values[0]]==andAnotherCustomID;]
  `
});



/* 
We use "$onlyIf[$interactionData[values[0]]==customID;]" to make sure this only will be triggered for the according select menu option.

Also ensure that you have the "onMessage" event in your main file (index.js in most cases).
*/
```

Handler Example

```js
module.exports = [{
    name: "add-select-menu",
    code: `
     Select an option.
     $addSelectMenu[1;yourCustomID;This is a placeholder!;1;1;false;A Option:Description of option B:anotherCustomID:false;B Option:Description of option B:andAnotherCustomID:true]
  `
}, {
    name: "yourCustomID",
    type: "interaction", // clarifying that this command is an Interaction
    prototype: "selectMenu",
    code: `
     $interactionReply[Hello! :);;;;everyone;false]
     $onlyIf[$interactionData[values[0]]==anotherCustomID;]`
}, {
    name: "yourCustomID",
    type: "interaction", // clarifying that this command is an Interaction
    prototype: "selectMenu", 
    code: `
     $interactionReply[Bye! :(;;;;everyone;false]
     $onlyIf[$interactionData[values[0]]==andAnotherCustomID;]`
}]
```

[dp]: https://discord.com/developers/docs/interactions/message-components#button-object-button-styles

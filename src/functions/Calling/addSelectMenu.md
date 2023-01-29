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



## Example

This adds a primary and link button to the bot's message:

```javascript
bot.command({
  name: "add-select-menu",
  code:`
  Select an option.
  
  $addSelectMenu[1;helpCustomID;This placeholder won't show up cause we have selected default field as yes;1;1;no;A Option:Description of A option:Example2:no:👋;B Option::Example1:true]
  `
});

bot.interactionCommand({
  name: "helpCustomID",
  prototype: "selectMenu", 
  code: `
  $interactionUpdate[A option's response.;;{actionRow:{selectMenu:helpCustomID:Menu has been disabled:1:1:true:{selectMenuOptions:This won't show up:Example2:Either this.:false}{selectMenuOptions:This won't show up either.:Example1:cause menu disabled.:false}}}]
  $onlyIf[$interactionData[values[0]]==Example2;]
  `
});

bot.interactionCommand({
  name: "helpCustomID",
  prototype: "selectMenu", 
  code: `
  $interactionUpdate[B option's response.;;{actionRow:{selectMenu:helpCustomID:Menu has been disabled:1:1:true:{selectMenuOptions:This won't show up:Example2:Either this.:false}{selectMenuOptions:This won't show up either.:Example1:cause menu disabled.:false}}}]

  $onlyIf[$interactionData[values[0]]==Example1;]
  `
});
```

[dp]: https://discord.com/developers/docs/interactions/message-components#button-object-button-styles

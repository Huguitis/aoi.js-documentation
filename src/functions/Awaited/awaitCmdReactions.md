---
title: $awaitCmdReactions 
description: $awaitCmdReactions will reply when a user reacts to a message with a specific emoji.
id: awaitCmdReactions
---

`$awaitCmdReactions` will reply when a user reacts to a message with a specific emoji.

## Usage

```php
$awaitCmdReactions[userfilter;time;reactions;commands;errorMsg?;awaitData?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| userfilter   | string  | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID  | yes      |
| time    | integer  | how long the command will last / when the command expires| yes      |
| reactions    | string  | reactions the bot will be listening to, you can seperate multiple emojis with a comma ( `,` )                             | yes      |
| commands    | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )                               | yes      |
| errorMsg    | string  | error message when command expires                             | no      |
| awaitData    | string  | awaited data                             | no      |


#### Make sure you have `GuildMessageReactions` as intent in your main file.

## Example

This will reply to you when you react with the "❤️" emoji:

```js
bot.command({
  name: "awaitCmdReaction",
  code: `
  React with "❤️" for a surprise! 
  $awaitCmdReactions[$authorID;10s;❤️;awaitedCommandExample;Whoops! You didn't react in time..]
  `
});

bot.awaitedCommand({
  name: "awaitedCommandExample",
  code: `
  Nice, you reacted with ❤️.
  `
});
```

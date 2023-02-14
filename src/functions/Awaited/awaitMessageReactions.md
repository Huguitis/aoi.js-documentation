---
title: $awaitMessageReactions 
description: $awaitMessageReactions will reply when a user reacts with a specific emoji.
id: awaitMessageReactions
---

`$awaitMessageReactions` will reply when a user reacts with a specific emoji.

## Usage

```php
$awaitMessageReactions[channelID;messageID;userFilter;time;reactions;commands;errorMessage?;awaitData?]
```

## Parameters 


| Field         | Type    | Description                                                                                    | Required |
|---------------|---------|------------------------------------------------------------------------------------------------|:--------:|
| channelID     | integer | message ID                                                                                     |   true    |
| messageID     | integer | message ID                                                                                     |   true    |
| userFilter    | string  | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID |   true    |
| time          | string  | how long the command will last / when the command expires                                      |   true    |
| reactions     | string  | reactions, you can add multiple by seperating them with commas ( `,` )                         |   true    |
| commands      | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )          |   true    |
| errorMessage? | string  | error message when command expires                                                             |    false    |
| awaitData?    | string  | awaited data                                                                                   |    false    |

#### Make sure you have `GuildMessageReactions` as intent in your main file.

## Example

This will reply to you when you react with the "❤️" emoji to the bot's message:

```js
bot.command({
  name: "awaitMessageReactions",
  code: `
  React with "❤️" for a surprise! 
  $awaitMessageReactions[$channelID;$messageID;$authorID;10s;❤️;awaitedCommandExample;Whoops! You didn't react in time..]
  `
});

bot.awaitedCommand({
  name: "awaitedCommandExample",
  code: `
  Nice, you reacted with ❤️.
  `
});
```

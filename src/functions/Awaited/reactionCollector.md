---
title: $reactionCollector 
description: $reactionCollector will create a reaction collector on a given message.
id: reactionCollector
---

`$reactionCollector` will create a reaction collector on a given message.

## Usage

```php
$reactionCollector[channelID;messageID;userFilters;time;reactions;awaits;removeReaction?;awaitData?;endAwait?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| channelID    | integer  | channel ID | yes      |
| messageID    | integer  | message ID | yes      |
| userfilter   | string  | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID  | yes      |
| time    | string  | when the command expires                               | yes      |
| reactions?    | string  | reactions, you can seperate multiple emojis with a comma ( `,` )                                | yes      |
| awaits?    | string  | commands to execute, you can seperate multiple emojis with a comma ( `,` )                              | yes      |
| removeReaction?    | string  | remove the reactions after the commands executed                             | no      |
| data?    | string  | awaited data                             | no      |
| endAwait?    | integer  | error message when command expires                             | no      |


## Example

This will send a message when you add a reaction:

```js
bot.command({
  name: "reactionCollector",
  code: `
  $reactionCollector[$channelID;$splitText[1];$authorID;10m;👀;awaitReaction;yes]
  $textSplit[$sendMessage[React with "👀" for something special!;yes]; ]
  `
});

bot.awaitedCommand({
  name: "awaitReaction",
  code: `
  $sendMessage[👀 what's this?]
  `
});
```


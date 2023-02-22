---
title: $awaitMessages
description: $awaitMessages will reply once a given message has been sent by the given user.
id: awaitMessages
---

`$awaitMessages` will reply once a given message has been sent by the given user.

## Usage

```php
$awaitMessages[channelID;userFilter;time;replies;cmds;errorMessage?;awaitData?;dm?]
```

## Parameters

| Field         | Type    | Description                                                                                                                        | Required |
|---------------|---------|------------------------------------------------------------------------------------------------------------------------------------|:--------:|
| channelID     | integer | channel ID                                                                                                                         |   true   |
| userFilter    | integer | user filter <br /> 1. **everyone** <br /> 2. **specific user** - any user ID                                                       |   true   |
| time          | string  | how long the command lasts / when it expires                                                                                       |   true   |
| replies       | string  | to what the bot will be reponding to, multiple words can be seperated with a comma  (or use "everything" to respond to everything) |   true   |
| cmds          | string  | commands that will be executed, multiple commands can be seperated with a comma                                                    |   true   |
| errorMessage? | string  | error message when the command expires                                                                                             |  false   |
| awaitData?    | string  | awaited Data                                                                                                                       |  false   |
| dm?           | string  | if the command will be executed in DMs or not                                                                                      |  false   |

## Example

This will reply to any message you send after executing the command:

```js
bot.command({
    name: "awaitMessages",
    code: `
  $awaitMessages[$channelID;$authorID;15s;everything;awaitedcommandexample;Oh? You don't want to talk to me..?] 
  What's your name?
  `
    // Please make sure that the awaitedCommand name is ALL lowercase of it won't work.
});

bot.awaitedCommand({
    name: "awaitedcommandexample",
    code: `
  Nice to meet you, $message!
  `
});
```

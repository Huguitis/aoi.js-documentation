---
title: Interaction Commands 
description: Everything you need to know about slash commands.
id: intcommands
---

## Interaction Commands

### Table of Content
  - **[Introduction][introduction]**
  - **[Getting Started][getting-started]**
     - **[Inviting your bot with correct permissions][getting-started-sub-inviting-your-bot-with-correct-permissions]**
     - **[Discord Developer Portal - Documentation][3]**
  - **[Important][important]**
  - **[Creating Application Commands][creating-application-commands]**
  - **[Using Application Commands][using-application-commands]**
  - **[Application Command Option Type][application-command-option-type]**
     - **[Discord Developer Portal - Documentation][4]**
  - **[Interaction Functions][interaction-functions]**
---

## Introduction

Slash Commands are the new and exciting way to create and interact with applications on Discord. With Slash Commands, all you need to do is type `/` and you'll be able to use your favourite bot. Users can easily learn what your bot can do, and discover new features as they are added. Validation, error states, and user-friendly interface guides them through your commands, so they can get it right the first time, especially on mobile. You now have an additional tool to combat your phone's autocorrect. Slash Commands set your users up for success instead of confusion and frustration. They separate how users think and how your code works, meaning no matter how complex your codebase and commands may become, people who love your bot will find it easy to use and accessible.

![slash](https://cdn.discordapp.com/attachments/1061712111052521493/1062518328268169306/image_4.png)

## Getting Started
### Inviting your bot with correct permissions

In order to use Application Commands, your bot needs the `application.commands` scope which can be found on the [Discord Developer Portal](https://discord.com/developers/applications/). You don't have to kick your bot or anything, simply reinvite it.

![scope](https://media.discordapp.net/attachments/1061712111052521493/1062539303386873929/image_5.png?width=1200&height=447)

## Important

* Due to Discord's Limitation you can only have up to **50 slash commands** in your bot / per guild.
* Two Application commands can **not have the same name** in the same guild.
* Application command names can **not contain special symbols** and must be shorter than **32 characters**.
* You require `bot.onInteractionCreate();` in your main file.

![slash.example](https://cdn.discordapp.com/attachments/1061712111052521493/1062559509601591427/image_6.png)

## Creating Application Commands

```js
$createApplicationCommand[guildID/global;name;description;defaultPermission(true/false);type(slash/user/message) (optional);options (optional)]
```

```js
bot.command({
  name: "createApplicationCommand",
  code: `
  $createApplicationCommand[$guildID/global;example;slash command description!;true;slash]`
});
/* Will create a slash commands without any user input, you can choose between global/$guildID to create a command globally or only for a specific guild.
Example created by dodoGames#7509. */
```
Adding **choices** to the application command:
```js
bot.command({
  name: "createApplicationCommand",
  code: `
  $createApplicationCommand[$guildID;choice;slash command choices showcase!;true;slash;[{
  "name": "option",
  "description": "options example",
  "required": true,
  "type": 3,
"choices" : [{
"name" : "test1",
"value" : "value1"
},{
"name" : "test2",
"value" : "value2"
},{
"name" : "test3",
"value" : "value3"
}]
}]`
});
/* You can choose between global/$guildID to create a command globally or only for a specific guild.
Example created by dodoGames#7509. */
```

Adding **sub command groups** to the application command:
```js
bot.command({
  name: "createApplicationCommand",
  code: `
  $createApplicationCommand[$guildID;slash;sub commands showcase!;true;slash;[
  {
  "name": "sub1",
  "description": "an sub command example!",
  "type": 1,
  "options": [
       {
          "name": "user", 
          "description": "example option", 
          "required": true, 
          "type": 6
        }
        ]
}]`
});
/* You can choose between global/$guildID to create a command globally or only for a specific guild.
Example created by dodoGames#7509. */
```

## Using Application Commands

To use application commands you require `interaction` commands.

Main file:
```js
bot.interactionCommand({
  name: "slash command name", //name of the slash command
  prototype : "slash", //clarifying that this command belongs to a slash command 
  code: `code` // code that will be executed if slash command triggered
});
```

Command Handler:
```js
module.exports = [{
  name: "slash command name", //name of the slash command
  prototype : "slash", //clarifying that this command belongs to a slash command 
  type: "interaction", //clarifying that this command is an interaction command
  code: `code` // code that will be executed if slash command triggered
}]
```

You can retrive information given in slash commands by using `$slashOption[slashcommandoptionname]`.

```js
$createApplicationCommand[$guildID;say;say command;true;slash;[{
  "name": "text",
  "description": "Text you want to say!",
  "required": true,
  "type": 3
+}]
// make sure to eval the code above
```
```js
module.exports = [{
  name: "say",
  prototype : "slash",
  type: "interaction", 
  code: `$interactionReply[You said: $slashOption[text]!]`
}]
```

## [Application Command Option Type](https://discord.com/developers/docs/interactions/application-commands#application-command-object-application-command-option-type)

| NAME              | ID | NOTE                                                                                         |
|-------------------|----|----------------------------------------------------------------------------------------------|
| SUB_COMMAND       | 1  |                                                                                              |
| SUB_COMMAND_GROUP | 2  |                                                                                              |
| STRING            | 3  |                                                                                              |
| INTEGER           | 4  | Any Integer between -2^53 and 2^53                                                           |
| BOOLEAN           | 5  |                                                                                              |
| USER              | 6  |                                                                                              |
| CHANNEL           | 7  | Includes all channel types + categories                                                      |
| ROLE              | 8  |                                                                                              |
| MENTIONABLE       | 9  | Includes users and roles                                                                     |
| NUMBER            | 10 | Any double between -2^53 and 2^53                                                            |
| ATTACHMENT        | 11 | [attachment](https://discord.com/developers/docs/resources/channel#attachment-object) object |

## Interaction Functions
* **[$interactionReply[message;embeds?;components?;files?;ephemeral(yes/no)]](../src/functions/events/interactionReply.md)**
* **[$interactionDefer[ephemeral]](../src/functions/events/interactionDefer.md)**
* **[$interactionDeferUpdate[ephemeral]](../src/functions/events/interactionDeferUpdate.md)**
* **[$interactionDelete](../src/functions/events/interactionDelete.md)**
* **[$interactionEdit[content?;embeds?;components?;files?;allowed mentions?]](../src/functions/events/interactionEdit.md)**
* **[$interactionFollowUp[content?;embeds?;components?;files?;ephemeral?]](../src/functions/events/interactionFollowUp.md)**
* **[$interactionUpdate[content?;embeds?;components?;files?;allowed mentions?]](../src/functions/events/interactionUpdate.md)**
* **[$slashOption[option]](../src/functions/events/interactionUpdate.md)**
* **$deleteSlashCommand[guildID/global;id]**
* **$modifyApplicationCommand[guildID/global;commandID;name;description;type(optional);options (optional);defaultPermission(optional)]**
* **$getApplicationCommandOptions[name;guildID/global (optional : global as default)]**
* **$getApplicationCommandID[name;guildID/global (optional : global as default)]**

<!--- links -->
[introduction]: #introduction
[getting-started]: #getting-started
[getting-started-sub-inviting-your-bot-with-correct-permissions]: #inviting-your-bot-with-correct-permissions
[important]: #important
[creating-application-commands]: #creating-application-commands
[using-application-commands]: #using-application-commands
[application-command-option-type]: #application-command-option-type
[interaction-functions]: #interaction-functions
[3]: https://discord.com/developers/docs/topics/gateway#list-of-intents
[4]: https://discord.com/developers/docs/interactions/application-commands#application-command-object-application-command-option-type

---
title: $awaitCmdReactions 
description: $awaitCmdReactions will reply when a user reacts to a message with a specific emoji.
id: awaitCmdReactions
---

`$awaitCmdReactions` will reply when a user reacts to a message with a specific emoji.

## Usage

```php
$awaitComponentsUntil[channelID;messageID;filter;time;customIDs;commands;errorMessage?;data?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| channelID   | string  | channel ID  | yes      |
| messageID   | string  | message ID  | yes      |
| filter    | integer  | to what the bot will reply <br> 1. **everyone** <br> 2. **specific user ID** - any user ID | yes      |
| reactions    | string  | reactions the bot will be listening to, you can seperate multiple emojis with a comma ( `,` )     | yes      |
| commands    | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )        | yes      |
| errorMsg    | string  | error message when command expires                             | no      |
| awaitData    | string  | awaited data                             | no      |

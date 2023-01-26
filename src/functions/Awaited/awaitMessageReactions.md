---
title: $awaitMessageReactions 
description: $awaitMessageReactions will reply when a user reacts with a specific emoji.
id: awaitMessageReactions
---

`$awaitMessageReactions` will reply when a user reacts with a specific emoji.

## Usage

```php
$awaitMessageReactions[channelID;messageID;filter;time;reactions;commands;errorMessage?;data?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| channelID    | integer  | message ID | yes      |
| messageID    | integer  | message ID | yes      |
| filter   | string  | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID  | yes      |
| time   | string  | how long the command will last / when the command expires  | yes      |
| reactions    | string  | reactions, you can add multiple by seperating them with commas ( `,` )                           | yes      |
| commands    | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )                               | yes      |
| errorMessage?    | string  | error message when command expires                             | no      |
| data?    | string  | awaited data                             | no      |

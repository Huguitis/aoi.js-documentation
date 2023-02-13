---
title: $awaitComponentsUntil 
description: $awaitComponentsUntil awaits message components.
id: awaitComponentsUntil
---

`$awaitComponentsUntil` awaits message components.

## Usage

```php
$awaitComponentsUntil[channelID;messageID;userFilter;time;customIDs;commands;errorMessage?;data?]
```

## Parameters 


| Field      | Type    | Description                                                                                    | Required |
|------------|---------|------------------------------------------------------------------------------------------------|:--------:|
| channelID  | string  | channel ID                                                                                     |   yes    |
| messageID  | string  | message ID                                                                                     |   yes    |
| userFilter | integer | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID |   yes    |
| reactions  | string  | reactions the bot will be listening to, you can seperate multiple emojis with a comma ( `,` )  |   yes    |
| commands   | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )          |   yes    |
| errorMsg   | string  | error message when command expires                                                             |    no    |
| awaitData  | string  | awaited data                                                                                   |    no    |

---
title: $awaitComponentsUntil
description: $awaitComponentsUntil awaits message components.
id: awaitComponentsUntil
---

`$awaitComponentsUntil` awaits message components until a specific time and makes in unuseable after that time.

## Usage

```php
$awaitComponentsUntil[channelID;messageID;userFilter;time;customIDs;commands;errorMsg?;awaitData?]
```

## Parameters

| Field      | Type    | Description                                                                                    | Required |
|------------|---------|------------------------------------------------------------------------------------------------|:--------:|
| channelID  | string  | channel ID                                                                                     |   true   |
| messageID  | string  | message ID                                                                                     |   true   |
| userFilter | integer | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID |   true   |
| reactions  | string  | reactions the bot will be listening to, you can seperate multiple emojis with a comma ( `,` )  |   true   |
| commands   | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )          |   true   |
| errorMsg?  | string  | error message when command expires                                                             |  false   |
| awaitData? | string  | awaited data                                                                                   |  false   |
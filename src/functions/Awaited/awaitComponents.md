---
title: $awaitComponents
description: $awaitComponents awaits components for given amount of uses.
id: awaitComponents
---

`$awaitComponents` awaits components for given amount of uses.

## Usage

```php
$awaitComponents[messageID;userFilter;customID;commands;errorMsg?;uses?;awaitData?]
```

## Parameters

| Field      | Type    | Description                                                                                    | Required |
|------------|---------|------------------------------------------------------------------------------------------------|:--------:|
| messageID  | integer | message ID                                                                                     |   true   |
| userFilter | string  | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID |   true   |
| customID   | string  | custom ID                                                                                      |   true   |
| commands   | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )          |   true   |
| errorMsg?  | string  | error message when command expires                                                             |  false   |
| uses?      | integer | how many uses until component stops working                                                    |  false   |
| awaitData? | string  | awaited data                                                                                   |  false   |
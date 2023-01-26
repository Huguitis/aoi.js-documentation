---
title: $awaitComponents 
description: $awaitComponents awaits button for given amount of uses.
id: awaitComponents
---

`$awaitComponents` awaits button for given amount of uses.

## Usage

```php
$awaitComponents[messageID;userFilter;customID;commands;errorMsg?;uses?;data?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| messageID    | integer  | message ID | yes      |
| userfilter   | string  | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID  | yes      |
| customID    | string  | custom ID                            | yes      |
| commands    | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )                               | yes      |
| errorMsg?    | string  | error message when command expires                             | no      |
| uses?    | integer  | error message when command expires                             | no      |
| data?    | string  | awaited data                             | no      |

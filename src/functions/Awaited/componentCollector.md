---
title: $componentCollector 
description: $componentCollector will create a collector for the given components.
id: componentCollector
---

`$componentCollector` will create a collector for the given components.

## Usage

```php
$componentCollector[messageID;userFilter;time;customIDs;commands;errorMsg?;endcommand?;awaitData?]
```

## Parameters

| Field       | Type    | Description                                                                                    | Required |
| ----------- | ------- | ---------------------------------------------------------------------------------------------- |:--------:|
| messageID   | integer | message ID                                                                                     |    yes   |
| userFilter  | string  | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID |    yes   |
| time        | string  | when the command ends/expires                                                                  |    yes   |
| customID    | string  | custom ID                                                                                      |    yes   |
| commands    | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )          |    yes   |
| errorMsg?   | string  | error message when command expires                                                             |    no    |
| endcommand? | integer | end command                                                                                    |    no    |
| data?       | string  | awaited data                                                                                   |    no    |

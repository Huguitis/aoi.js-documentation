---
title: $componentCollector 
description: $componentCollector will create a collector for the given customIDs.
id: componentCollector
---

`$componentCollector` will create a collector for the given customIDs.

## Usage

```php
$componentCollector[messageID;filter;time;customIDs;commands;errorMsg?;endcommand?;awaitData?]
```

## Parameters

| Field       | Type    | Description                                                                                    | Required |
| ----------- | ------- | ---------------------------------------------------------------------------------------------- |:--------:|
| messageID   | integer | message ID                                                                                     |    yes   |
| userfilter  | string  | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID |    yes   |
| time        | string  | when the command ends/expires                                                                  |    yes   |
| customID    | string  | custom ID                                                                                      |    yes   |
| commands    | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )          |    yes   |
| errorMsg?   | string  | error message when command expires                                                             |    no    |
| endcommand? | integer | end command                                                                                    |    no    |
| data?       | string  | awaited data                                                                                   |    no    |

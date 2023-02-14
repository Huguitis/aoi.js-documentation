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
| messageID   | integer | message ID                                                                                     |    true   |
| userFilter  | string  | to what the bot will reply <br /> 1. **everyone** <br /> 2. **specific user ID** - any user ID |    true   |
| time        | string  | when the command ends/expires                                                                  |    true   |
| customID    | string  | custom ID                                                                                      |    true   |
| commands    | string  | commands that will be executed, you can seperate multiple emojis with a comma ( `,` )          |    true   |
| errorMsg?   | string  | error message when command expires                                                             |    false    |
| endcommand? | integer | end command                                                                                    |    false    |
| data?       | string  | awaited data                                                                                   |    false    |

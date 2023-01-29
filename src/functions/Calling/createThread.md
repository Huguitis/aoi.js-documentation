---
title: $createThread 
description: $createThread will create a new thread.
id: createThread
---

`$createThread` will create a new thread.

## Usage

```php
$createThread[channelID;name;archive;type;startMessage;returnId?]
```

## Parameters 


| Field        | Type    | Description                                                                    | Required |
| ------------ | ------- | ------------------------------------------------------------------------------ |:--------:|
| channelID    | integer | guild ID                                                                       |    yes   |
| name         | string  | thread name                                                                    |    yes   |
| archieve     | string  | achieve after how much time <br /> 1. **MAX** (default) <br /> 2. *time in ms* |    yes   |
| type         | string  | thread type <br /> 1. **1** - public (default) <br /> 2. **2** - private       |    yes   |
| startMessage | string  | thread start message ID                                                        |    yes   |
| returnId?    | string  | return thread ID                                                               |    no    |


## Example

This will create a thread in the current channel:

```javascript
bot.command({
  name: 'createThread',
  code: `
  $createThread[$channelID;Example!;MAX;1;$messageID;false]
  `
});
```

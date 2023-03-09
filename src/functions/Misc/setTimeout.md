---
title: $setTimeout
description: $setTimeout will set a timeout for a given action (which will even continue to run after bot restart).
id: setTimeout
---

`$setTimeout` will set a timeout for a given action (which will even continue to run after bot restart).

## Usage

```php
$setTimeout[name;duration;timeoutData;returnId?;pulse?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| name    | string   | awaited command name                                                         |   true   |
| duration    | string, number   | after how much time it will execute / this cannot go over **21 days** |   true   |
| timeoutData    | integer   | timeout data                                                         |   true   |
| returnId?    | string   | return message ID                                                         |   false   |
| pulse?    | number   | delay                                                         |   false   |

You can retrieve timeout data using `$timeoutData[name]`.
* Note that the duration may not go over **21 days**.

## Example

This will send "Hello!" after 10 seconds in the command execution channel:

```javascript
bot.command({
    name: "setTimeout", 
    code: `
    $setTimeout[timeoutCommand;10s;{"channelID": "$channelID", "authorID": "$authorID"};false]
    `
});

bot.timeoutCommand({
    name: "timeoutCommand",
    code: `
    $channelSendMessage[$timeoutData[channelID];Hello, <@$timeoutData[authorID]>!]
    `
});
```
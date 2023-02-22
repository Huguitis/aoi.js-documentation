---
title: $deleteThread
description: $deleteThread will delete a thread of a channel.
id: deleteThread
---

`$deleteThread` will delete a thread of a channel.

## Usage

```php
$deleteThread[channelID;threadID;reason?]
```

## Parameters

| Field     | Type    | Description                                  | Required |
|-----------|---------|----------------------------------------------|:--------:|
| channelID | integer | ID of the channel where the thread exists in |   true   |
| threadID  | integer | thread ID                                    |   true   |
| reason?   | string  | guild ID                                     |  false   |

## Example

This will delete a thread of the channel where you execute the command in ( make sure to replace threadID with an actual
thread ID ):

```javascript
bot.command({
    name: 'deleteThread',
    code: `
  $deleteThread[$channelID;threadID;Crazy Example.]
  `
});
```
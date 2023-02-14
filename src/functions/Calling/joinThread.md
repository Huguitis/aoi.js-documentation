---
title: $joinThread 
description: $joinThread will make the bot join a specific thread.
id: joinThread
---

`$joinThread` will make the bot join a specific thread.

## Usage

```php
$joinThread[channelID;threadID]
```

## Parameters 


| Field     | Type    | Description | Required |
| --------- | ------- | ----------- |:--------:|
| channelID | integer | channel ID  |    yes   |
| threadID  | integer | thread ID   |    yes   |

## Example

This will create a thread in the current channel and add the bot to it:

```javascript
bot.command({
  name: 'joinThread',
  code: `
  $joinThread[$get[threadID]]
  $let[threadID;$createThread[$channelID;Example!;1440;public;$messageID;yes]]
  `
});
```
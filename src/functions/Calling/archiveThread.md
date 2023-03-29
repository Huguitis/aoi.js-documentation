---
title: $archiveThread
description: $archiveThread will archive or unarchive a specific thread.
id: archiveThread
---

`$archiveThread` will archive or unarchive a specific thread.

## Usage

```php
$archiveThread[threadID;channelID?;archive?;reason?]
```

## Parameters

| Field      | Type    | Description                     | Required |
|------------|---------|---------------------------------|:--------:|
| threadID   | integer | thread ID                       |   true   |
| channelID? | integer | channel ID                      |  false   |
| archive?   | integer | archive thread?                 |  false   |
| reason?    | string  | reason to display in audit logs |  false   |

## Example(s)

This will archive the created thread:

```javascript
bot.command({
    name: 'archiveThread',
    code: `
  $archiveThread[$channelID;$get[id];true;testing]
  $let[id;$createThread[$channelID;example;1440;public;$messageID;true]]  
  `
});
```

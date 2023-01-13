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


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| threadID    | integer  | thread ID                             | yes      |
| channelID?    | integer  | channel ID                             | no      |
| archive?    | integer  | yes/no                             | no      |
| reason?    | string  | reason to display in audit logs                             | no      |


## Example

This will archive the created thread:

```javascript
bot.command({
  name: 'archiveThread',
  code: `
  $archiveThread[$channelID;$get[id];yes;testing]
  $let[id;$createThread[$channelID;example;1440;public;$messageID;yes]]  
  `
});
```

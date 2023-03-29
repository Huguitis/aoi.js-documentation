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

| Field        | Type    | Description                                                      | Required |
|--------------|---------|------------------------------------------------------------------|:--------:|
| channelID    | integer | guild ID                                                         |   true   |
| name         | string  | thread name                                                      |   true   |
| achieve      | string  | achieve after how much time  <br /> 1. *time in ms*              |   true   |
| type         | string  | thread type <br /> 1. **public** (default) <br /> 2. **private** |   true   |
| startMessage | string  | thread start message ID                                          |   true   |
| returnId?    | string  | return thread ID                                                 |  false   |

* **60 —** This option makes the thread stays active for **1 hour**.
* **1140 —** This option makes the thread stays active for **1 day**.
* **4320 —** This option makes the thread stays active for **3 days**.
* **10080 —** This option makes the thread stays active for **1 week**.

## Example(s)

This will create a thread in the current channel:

```javascript
bot.command({
    name: 'createThread',
    code: `
  $createThread[$channelID;Example!;60;public;$messageID;false]
  `
});
```

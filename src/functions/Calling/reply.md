---
title: $reply
description: $reply will reply to a given message.
id: reply
---

`$reply` will reply to a given message.

## Usage

```php
$reply[messageID?;mentionUser?]
```

## Parameters

| Field        | Type    | Description                                                                     | Required |
|--------------|---------|---------------------------------------------------------------------------------|:--------:|
| messageID?   | integer | message ID                                                                      |  false   |
| mentionUser? | string  | mention the user in the reply <br /> 1. **true** (default)  <br /> 2. **false** |  false   |

## Example

This will reply to your command message:

```javascript
bot.command({
    name: 'reply',
    code: `
   Hello!
   $reply[$messageID;true]
  `
});
```
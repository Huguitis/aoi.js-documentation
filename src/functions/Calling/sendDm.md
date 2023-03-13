---
title: $sendDm
description: $sendDm will Direct Message a given user.
id: sendDm
---

`$sendDm` will Direct Message a given user.

## Usage

```php
$sendDm[message;userID?;returnID?]
```

## Parameters 

| Field     | Type   | Description                                                         | Required |
|-----------|--------|---------------------------------------------------------------------|:--------:|
| message   | string | message to send                                                     |   true   |
| userID?   | string | user which receives the DM                                          |  false   |
| returnID? | string | return message ID  <br /> 1. **true** <br /> 2. **false** (default) |  false   |

## Example

This will send a DM to the command author:

```javascript
bot.command({
    name: 'sendDm',
    code: `
   $sendDm[Hello!;$authorID;false]  
  `
});
```
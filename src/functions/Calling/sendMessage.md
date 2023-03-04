---
title: $sendMessage
description: $sendMessage will send a message in the execution channel.
id: sendMessage
---

`$sendMessage` will send a message in the execution channel.

## Usage

```php
$sendMessage[message;returnID?]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| message  | string | message to send        |   true   |
| returnID?  | string | return message ID  <br /> 1. **true** <br /> 2. **false** (default)       |   false   |

## Examples

This will send a message in the current channel:

```javascript
bot.command({
    name: 'sendMessage',
    code: `
   $sendMessage[Hello!;false]  
  `
});
```

This will send an embed in the current channel using parsers:

```javascript
bot.command({
    name: 'sendMessage',
    code: `
   $sendMessage[Hello! {newEmbed:{title:Bonjour!}};false]  
  `
});
```
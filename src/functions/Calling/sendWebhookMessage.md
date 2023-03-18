---
title: $sendWebhookMessage
description: $sendWebhookMessage will send a message using an existing webhook.
id: sendWebhookMessage
---

`$sendWebhookMessage` will send a message using an existing webhook.

## Usage

```php
$sendWebhookMessage[webhookID;webhookToken;message;returnID?]
```

## Parameters

| Field        | Type    | Description                                                         | Required |
|--------------|---------|---------------------------------------------------------------------|:--------:|
| webhookID    | integer | webhook ID                                                          |   true   |
| webhookToken | string  | webhook Token                                                       |   true   |
| message      | string  | message to send                                                     |   true   |
| returnID?    | string  | return message ID  <br /> 1. **true** <br /> 2. **false** (default) |  false   |

## Example

This will create a webhook and send a message using it:

```javascript
bot.command({
    name: 'sendWebhookMessage',
    code: `
   $sendWebhookMessage[$splitText[1];$splitText[2];Hello!;false]
   $textSplit[$createWebhook[$channelID;$username;$userAvatar;Testing!;,];,]
  ` /* Using $textSplit to split the ID and Token in seperate parts to use it in sendWebhookMessage
  $splitText[1] equals the webhook ID 
  $splitText[2] equals the webhook Token
  */
});
```
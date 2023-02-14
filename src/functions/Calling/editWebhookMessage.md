---
title: $editWebhookMessage 
description: $editWebhookMessage will edit a given webhook message.
id: editWebhookMessage
---

`$editWebhookMessage` will edit a given webhook message.

## Usage

```php
$editWebhookMessage[webhookID;webhookToken;messageID;returnID?]
```

## Parameters 


| Field        | Type    | Description                                                         | Required |
| ------------ | ------- | ------------------------------------------------------------------- |:--------:|
| webhookID    | integer | message ID                                                          |    yes   |
| webhookToken | string  | new message                                                         |    yes   |
| messageID    | integer | channel ID                                                          |    yes   |
| returnID?    | string  | return the message ID? <br /> 1. **true** (default) <br /> 2. **false** |    no    |
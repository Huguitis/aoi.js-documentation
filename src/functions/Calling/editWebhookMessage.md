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

| Field        | Type    | Description                                                             | Required |
|--------------|---------|-------------------------------------------------------------------------|:--------:|
| webhookID    | integer | message ID                                                              |   true   |
| webhookToken | string  | new message                                                             |   true   |
| messageID    | integer | channel ID                                                              |   true   |
| returnID?    | string  | return the message ID? <br /> 1. **true** (default) <br /> 2. **false** |  false   |
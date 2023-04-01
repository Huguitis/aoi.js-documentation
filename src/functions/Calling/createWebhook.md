---
title: $createWebhook
description: $createWebhook will create a webhook.
id: createWebhook
---

`$createWebhook` will create a webhook.

## Usage

```php
$createWebhook[channelID;name;avatar;reason;separator?]
```

## Parameters

| Field      | Type    | Description                                             | Required |
|------------|---------|---------------------------------------------------------|:--------:|
| channelID  | integer | channel ID where the webhook will be created in         |   true   |
| name       | string  | webhook display name                                    |   true   |
| avatar     | string  | webhook avatar                                          |   true   |
| reason     | string  | reason that will be displayed in the guild's audit logs |   true   |
| separator? | string  | separator to separate webhook token, id, etc.           |  false   |

## Example(s)

This will create a webhook in the current channel:

```javascript
bot.command({
    name: 'createWebhook',
    code: `
  $createWebhook[$channelID;aoi.js is great;$userAvatar[$authorID];Just testing.;, ]
  `
});
```

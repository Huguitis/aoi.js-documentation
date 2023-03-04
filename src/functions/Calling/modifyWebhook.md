---
title: $modifyWebhook
description: $modifyWebhook will modify a given webhook.
id: modifyWebhook
---

`$modifyWebhook` will modify a given webhook.

## Usage

```php
$modifyWebhook[webhookID;name;avatar;channelID?;reason?]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| webhookID   | integer | webhook ID        |   true   |
| name        | string | new webhook name        |   true   |
| avatar  | string | new webhook avatar        |   true   |
| channelID?   | integer | ID of the channel where the webhook is located in        |   false   |
| reason?   | string | reason that will be displayed in the guilds audit logs        |   false   |

## Example

This will modify a existing webhook and change it's avatar to your user avatar:

```javascript
bot.command({
    name: 'modifyWebhook',
    code: `
  $modifyWebhook[webhookID;Hello!;$userAvatar[$authorID];$channelID;Testing!]
  `
});
```
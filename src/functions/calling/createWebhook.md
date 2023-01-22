---
title: $createWebhook 
description: $createWebhook will create a webhook.
id: createWebhook
---

`$createWebhook` will create a webhook.

## Usage

```php
$createWebhook[channelID;name;avatar;reason;separator]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| channelID    | integer  | channel ID where the webhook will be created in                             | yes      |
| name    | string  | webhook display name                             | yes      |
| avatar    | string  | webhook avatar                             | yes      |
| reason    | string  | reason that will be displayed in the guild's audit logs                             | yes      |
| seperator?    | string  | seperator to seperate webhook token, id, etc.                             | no      |


## Example

This will create a webhook in the current channel:

```javascript
bot.command({
  name: 'createWebhook',
  code: `
  $createWebhook[$channelID;aoi.js is great;$userAvatar[$authorID];Just testing.;, ]
  `
});
```

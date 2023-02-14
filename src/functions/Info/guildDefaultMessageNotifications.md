---
title: $guildDefaultMessageNotifications  
description: $guildDefaultMessageNotifications will return given guild's default message notification type.
id: guildDefaultMessageNotifications 
---

`$guildDefaultMessageNotifications ` will return given guild's default message notification type.

## Usage

```php
$guildDefaultMessageNotifications[guildID?]
```

## Parameters 


| Field    | Type    | Description                                                | Required |
| -------- | ------- | ---------------------------------------------------------- |:--------:|
| guildID? | integer | guild id you want the default message notification type of |    no    |


## Example

This will return the guild's default message notification type:

```javascript
bot.command({
  name: 'guildDefaultMessageNotifications',
  code: `
  $guildDefaultMessageNotifications
  `
});
```

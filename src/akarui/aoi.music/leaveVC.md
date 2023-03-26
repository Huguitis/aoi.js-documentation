---
title: $leaveVC
description: $leaveVC will make your bot leave the current Voice Channel.
id: leaveVC
---

`$leaveVC` will will make your bot leave the current Voice Channel.

## Usage

```php
$leaveVC[guildID?]
```

## Parameters

| Field    | Type    | Description | Required |
|----------|---------|-------------|:--------:|
| guildID? | integer | guild ID    |  false   |

## Example

This will make your bot leave the current voice channel in the current guild (if any):

```javascript
bot.command({
    name: 'leaveVC',
    code: `
    $leaveVC[$guildID]
  `
});
```
---
title: $channelPermissionsFor
description: $channelPermissionsFor will return the channel permissions of a specific user or role.
id: channelPermissionsFor
---

`$channelPermissionsFor` will return the channel permissions of a specific user or role.

## Usage

```php
$channelPermissionsFor[userorroleID?;channelID?;sep?]
```

## Parameters

| Field         | Type    | Description     | Required |
|---------------|---------|-----------------|:--------:|
| userorroleID? | integer | user or role ID |   true   |
| channelID?    | integer | channel ID      |   true   |
| sep?          | integer | guild ID        |   true   |

## Example(s)

This will return your permissions in the channel where you execute the command:

```javascript
bot.command({
    name: 'channelPermissionsFor',
    code: `
  $channelPermissionsFor[$authorID;$channelID;, ]
  `
});
```

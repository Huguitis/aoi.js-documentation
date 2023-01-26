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


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| userorroleID?    | integer  | user or role ID                             | yes      |
| channelID?    | integer  | channel ID                             | yes      |
| sep?    | integer  | guild ID                             | yes      |


## Example

This will return your permissions in the channel where you execute the command:

```javascript
bot.command({
  name: 'channelPermissionsFor',
  code: `
  $channelPermissionsFor[$authorID;$channelID;, ]
  `
});
```

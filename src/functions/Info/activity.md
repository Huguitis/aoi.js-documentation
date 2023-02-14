---
title: $activity 
description: $activity will return a user's activity.
id: activity
---

`$activity` will return a user's current activity.

## Usage

```php
$activity[guildID?;userID?]
```

## Parameters 


| Field    | Type    | Description | Required |
| -------- | ------- | ----------- | -------- |
| guildID? | integer | guild id    | false       |
| userID?  | integer | user id     | false       |


## Example

This will return your current Activity:

```javascript
bot.command({
  name: 'activity',
  code: `
  $activity[$guildID;$authorID]
  `
});
```
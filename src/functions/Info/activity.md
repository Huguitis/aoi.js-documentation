---
title: $activity 
description: $activity will return a user activity.
id: activity
---

`$activity` will return a user current activity.

## Usage

```php
$activity[guildID;id?]
```

## Parameters 


| Field  | Type    | Description | Required |
| ------ | ------- | ----------- | -------- |
| guildID? | integer | guild id    | yes       |
| id?    | integer | user id     | no      |


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
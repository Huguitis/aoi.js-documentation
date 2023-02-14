---
title: $memberJoinPosition 
description: $memberJoinPosition will return a members join position.
id: memberJoinPosition
---

`$memberJoinPosition` will return a members join position.

## Usage

```php
$memberJoinPosition[userID?;guildID?]
```

## Parameters 


| Field    | Type    | Description          | Required |
| -------- | ------- | -------------------- |:--------:|
| userID?  | integer | the ID of the member |    false    |
| guildID? | integer | the ID of the guild  |    false    |


## Example

This will return your join position, if you're the owner then it'd be `1`:

```javascript
bot.command({
  name: 'memberJoinPosition',
  code: `
  $memberJoinPosition[$authorID;$guildID]
  `
});
```

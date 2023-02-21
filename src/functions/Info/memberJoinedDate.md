---
title: $memberJoinedDate 
description: $memberJoinedDate will return a members join date in MS.
id: memberJoinedDate
---

`$memberJoinedDate` will return a members join date in MS.

## Usage

```php
$memberJoinedDate[userID?;guildID?]
```

## Parameters 


| Field    | Type    | Description                                            | Required |
| -------- | ------- | ------------------------------------------------------ | :------: |
| userID?  | integer | the ID of the member                                   |    false    |
| guildID? | integer | the ID of the guild                                    |    false    |


## Example

This will return your join date in MS and parsed date:

```javascript
bot.command({
  name: 'memberJoinedDate',
  code: `
  $memberJoinedDate[$authorID;$guildID] -> $parseDate[$memberJoinedDate[$authorID;$guildID]]
  `
});
```

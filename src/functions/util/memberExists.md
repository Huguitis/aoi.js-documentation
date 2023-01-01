---
title: $memberExists 
description: $memberExists check if a given user is present in the given guild.
id: memberExists
---

`$memberExists` check if a given user is present in the given guild.

## Usage

```php
$memberExists[userid;guildid?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| userid      | integer  | id of the user you want to check if they're currently present in the given server                           | yes      |
| guildid?     | integer  | the server where the user is present in          | no       |


## Example

This will return `true` as you're currently in this guild:

```javascript
bot.command({
  name: 'memberExists',
  code: `
  $memberExists[$authorid;$guildid]
  `
});
```

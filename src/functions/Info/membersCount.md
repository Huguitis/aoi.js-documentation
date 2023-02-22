---
title: $membersCount
description: $membersCount will return a guild's member count.
id: membersCount
---

`$membersCount` will return a guild's member count.

## Usage

```php
$membersCount[guildID?;presence?;countBot?]
```

## Parameters

| Field     | Type    | Description                                                                                                                           | Required |
|-----------|---------|---------------------------------------------------------------------------------------------------------------------------------------|:--------:|
| guildID?  | integer | the ID of the guild                                                                                                                   |  false   |
| presence? | string  | the presence of the users <br /> 1. **all** (default) <br /> 2. **dnd** <br /> 3. **idle** <br /> 4. **offline** <br /> 5. **online** |  false   |
| countBot? | string  | count bots? <br /> 1. **true** (default) <br /> 2. **false**                                                                          |  false   |

## Example

This will return the amount of offline users (including bots) in your guild:

```javascript
bot.command({
    name: 'membersCount',
    code: `
  $membersCount[$guildID;offline;true]
  `
});
```

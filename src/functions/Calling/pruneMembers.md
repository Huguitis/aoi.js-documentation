---
title: $pruneMembers
description: $pruneMembers will kick all inactive users whose been inactive for a given amount of time.
id: pruneMembers
---

`$pruneMembers` will kick all inactive users whose been inactive for a given amount of time.

## Usage

```php
$pruneMembers[days?;guildID?;roleIds?;dry?;reason?;count?]
```

## Parameters 

| Field     | Type    | Description     | Required |
|-----------|---------|-----------------|:--------:|
| days?   | number | number of days to count prune for (1-30, 7 default) |   false   |
| guildID?  | integer | guild ID        |   false   |
| roleIds?   | integer, string | roles to include, splitted by commas        |   false   |
| dry?   | string | 1. **true** <br /> 2. **false** (default)        |   false   |
| reason?   | string | reason to display in the guilds audit logs        |   false   |
| count?   | string | return count of pruned members <br /> 1. **true** <br /> 2. **false** (default)        |   false   |

## Example

This will prune all members who have been inactive for 4 days and return the count of the pruned members that meet those requirements:

```javascript
bot.command({
    name: 'pruneMembers',
    code: `
   $pruneMembers[4;$guildID;$guildID;true;Pruning!;true]
  `
});
```
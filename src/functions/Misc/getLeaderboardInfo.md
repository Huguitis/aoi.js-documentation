---
title: $getLeaderboardInfo
description: $getLeaderboardInfo will return information about a given variable sorted in a leaderboard.
id: getLeaderboardInfo
---

`$getLeaderboardInfo` will return information about a given variable sorted in a leaderboard.

## Usage

```php
$getLeaderboardInfo[variable;id;type?;option?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| varname    | string   | variable name                                                         |   true   |
| id    | integer   | user/guild/channel id                                                         |   true   |
| type    | string   | variable type <br /> 1. **globalUser** <br /> 2. **user** <br /> 3. **server** <br /> 4. **channel** |   true   |
| option?    | string   | data to return <br /> 1. **top** (default) <br /> **value** |   false   |

## Example

This will return the position of the current guild:

```javascript
bot.command({
    name: "getLeaderboardInfo",
    code: `
    $getLeaderboardInfo[Example;$guildID;server;top]
    `
});
```
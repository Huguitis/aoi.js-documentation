---
title: $globalUserLeaderBoard
description: $globalUserLeaderBoard will return a leaderboard of a global user variable.
id: globalUserLeaderBoard
---

`$globalUserLeaderBoard` will return a leaderboard of a global user variable.

## Usage

```php
$globalUserLeaderBoard[variable;type?;custom?;list?;page?;table?]
```

## Parameters

| Field    | Type   | Description                                                                                               | Required |
|----------|--------|-----------------------------------------------------------------------------------------------------------|:--------:|
| variable | string | variable name                                                                                             |   true   |
| type     | string | in which order it will be returned <br /> 1. **asc** (ascending / default) <br /> 2. **dsc** (descending) |  false   |
| custom?  | string | formatting                                                                                                |  false   |
| list?    | number | how many to list                                                                                          |  false   |
| page?    | number | which page to list                                                                                        |  false   |
| table?   | string | variable table                                                                                            |  false   |

| Options        | Returns         |                                         |
|----------------|-----------------|-----------------------------------------|
| **{top}**      | number          | Returns the position of the user.       |
| **{username}** | string          | Returns the username.                   |
| **{tag}**      | string          | Returns the username and discriminator. |
| **{id}**       | integer         | Returns the user ID.                    |
| **{value}**    | number, integer | Returns the variable value.             |

## Example

This will returns a leaderboard of the "Example" variable:

```javascript
bot.command({
    name: "globalUserLeaderBoard",
    code: `
    $globalUserLeaderBoard[Example;asc;{top}) {username} : {value};10;1;main]
    `
});
```
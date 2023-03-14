---
title: $rawLeaderboard
description: $rawLeaderboard will return a leaderboard of the given type.
id: rawLeaderboard
---

`$rawLeaderboard` will return a leaderboard of the given type.

## Usage

```php
$rawLeaderboard[variable;order?;type?;custom?;list?;page?;table?]
```

## Parameters

| Field    | Type   | Description                                                                                               | Required |
|----------|--------|-----------------------------------------------------------------------------------------------------------|:--------:|
| variable | string | variable name                                                                                             |   true   |
| type     | string | variable type <br /> 1. **globalUser** <br /> 2. **user** <br /> 3. **server** <br /> 4. **channel**      |   true   |
| order    | string | in which order it will be returned <br /> 1. **asc** (ascending / default) <br /> 2. **dsc** (descending) |   true   |
| custom?  | string | formatting                                                                                                |  false   |
| list?    | number | how many to list                                                                                          |  false   |
| page?    | number | which page to list                                                                                        |  false   |
| table?   | string | variable table                                                                                            |  false   |

| Options     | Returns         |                                         |
|-------------|-----------------|-----------------------------------------|
| **{top}**   | number          | Returns the position of the user.       |
| **{name}**  | string          | Returns the username.                   |
| **{tag}**   | string          | Returns the username and discriminator. |
| **{id}**    | integer         | Returns the user ID.                    |
| **{value}** | number, integer | Returns the variable value.             |

## Example

This will return a leaderboard of the "Example" variable:

```javascript
bot.command({
    name: "rawLeaderboard",
    code: `
    $rawLeaderboard[Example;asc;globalUser;{top}) {username} : {value};10;1;main]
    `
});
```
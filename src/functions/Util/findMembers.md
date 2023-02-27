---
title: $findMembers
description: $findMembers will return all members with similar username.
id: findMembers
---

`$findMembers` will return all members with similar username.

## Usage

```php
$findMembers[query;limit?;type?;force?;res?]
```

## Parameters

| Field  | Type   | Description                                   | Required |
|--------|--------|-----------------------------------------------|----------|
| query  | string | query of the username the bot will search for | true     |
| limit? | number | the amount of results the bot will return     | false    |
| type?  | string | type of the search query                      | false    |
| force? | string |                                               | false    |
| res?   | string | the format the bot will return the results    | false    |

### Parameters for the `res` argument

* {position} -> returns the position
* {id} -> returns the user ID
* {username} -> returns the username
* {nick} -> returns the nickname
* {tag} -> returns the user discriminator

## Example

This will return twenty members with `Leref` in their username:

```javascript
bot.command({
    name: 'findMembers',
    code: `
  $findMembers[Leref;20;startsWith;true;{position}) {username}#{tag}]
  `
});
```

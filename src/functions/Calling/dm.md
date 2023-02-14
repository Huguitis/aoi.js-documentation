---
title: $dm 
description: $dm will send a message to an users Direct Messages.
id: dm
---

`$dm` will send a message to an users Direct Messages.

## Usage

```php
$dm[userID]
```

## Parameters 


| Field  | Type    | Description | Required |
| ------ | ------- | ----------- |:--------:|
| userID | integer | user ID     |    true   |


## Example

This will send an DM to you containing "Hello! Did you really think this works?":

```javascript
bot.command({
  name: 'dm',
  code: `
  Hello! Did you really think this works?
  $dm[$authorID]
  `
});
```
---
title: $roleCount 
description: $roleCount will return the guild's role count.
id: roleCount
---

`$roleCount` will return the guild's role count.

## Usage

```php
$roleCount[guildID?;fetchFirst?]
```

## Parameters 


| Field       | Type    | Description                                                                                | Required |
| ----------- | ------- | ------------------------------------------------------------------------------------------ |:--------:|
| guildID?    | integer | guild ID                                                                                   |    false    |
| fetchFirst? | number  | fetch the roles first before returning them?  <br /> 1. **true** <br /> 2. **false** (default) |    false    |


## Example

This will return the amount of roles of your guild:

```javascript
bot.command({
  name: 'roleCount',
  code: `
  $roleCount[$guildID;true]
  `
});
```

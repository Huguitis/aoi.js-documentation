---
title: $usersBanned 
description: $usersBanned will return the banned users of a guild.
id: usersBanned
---

`$usersBanned` will return the banned users of a guild.

## Usage

```php
$usersBanned[guildID?;force?;option?;sep?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| guildID?    | integer  | guild ID                             | no      |
| force?    | string  | 1. **yes** <br /> 2. **no** (default)                             | no      |
| option?    | string  | how to return the banned users <br /> 1. **id** (default) <br /> 1. **username** <br /> 1. **mention** | no      |
| sep?    | string  | seperator to seperate multiple arguments                            | no      |


## Example

This will return the banned users of your guild as mention in an embed:

```javascript
bot.command({
  name: 'usersBanned',
  code: `
$description[$usersBanned[$guildID;no;mention;, ]]
  `
});
```

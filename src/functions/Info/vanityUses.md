---
title: $vanityUses 
description: $vanityUses will return the uses of a vanity URL.
id: vanityUses
---

`$vanityUses` will return the uses of a vanity URL.

## Usage

```php
$vanityUses[guildID?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| guildID?    | integer  | guild ID                             | no      |


## Example

This will return the uses of your guild's vanity URL, if you have one:

```javascript
bot.command({
  name: 'vanityUses',
  code: `
  $vanityUses[$guildID]
  `
});
```

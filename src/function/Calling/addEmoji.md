---
title: $addEmoji 
description: $addEmoji will add an emoji to the given guild. If role IDs are given, the emoji will only be usable by users with one of provided role IDs
id: addEmoji
---

`$addEmoji` will add an emoji to the given guild. If role IDs are given, the emoji will only be usable by users with one of provided role IDs

## Usage

```php
$addEmoji[guildID;url;name;returnEmoji?;reason?;...roles?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| guildID    | integer  | guild ID                             | yes      |
| url    | integer  | valid image URL                             | yes      |
| name | integer  | emoji name                             | yes      |
| returnEmoji?    | integer  | return the created emoji?                             | no      |
| reason?    | integer  | reason which will be displayed in the guild's audit logs                             | no      |
| roles?    | integer  | useable by the given role only?                             | no      |


## Example

This will create an emoji:

```javascript
bot.command({
  name: 'addEmoji',
  code: `
  $addEmoji[$guildID;https://cdn.discordapp.com/emojis/1010320053687832586.webp?size=96&quality=lossless;leref;no]
  `
});
```

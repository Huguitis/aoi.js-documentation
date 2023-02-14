---
title: $memberAvatar 
description: $memberAvatar will return the profile picture of a guild member.
id: memberAvatar
---

`$memberAvatar` will return the profile picture of a guild member.

## Usage

```php
$memberAvatar[guildID?;userID?;size?;dynamic?;format?]
```

## Parameters 


| Field    | Type    | Description                                            | Required |
| -------- | ------- | ------------------------------------------------------ | :------: |
| guildID? | integer | the ID of the guild                                    |    false    |
| userID?  | integer | the ID of the member                                   |    false    |
| size?    | integer | the size of the image                                  |    false    |
| dynamic? | string  | dynamic image <br /> 1. **true** (default) <br /> 2. **false** |    false    |
| format?  | string  |                                                        |    false    |


## Example

This will return your profile picture:

```javascript
bot.command({
  name: 'memberAvatar',
  code: `
  $memberAvatar[$guildID;$authorID;2048;true;webp]
  `
});
```

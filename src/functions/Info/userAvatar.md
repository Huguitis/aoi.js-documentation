---
title: $userAvatar 
description: $userAvatar will return the profile picture of a specific user.
id: userAvatar
---

`$userAvatar` will return the profile picture of a specific user.

## Usage

```php
$userAvatar[userID?;size?;dynamic?;format?]
```

## Parameters 


| Field    | Type    | Description                                                    | Required |
| -------- | ------- | -------------------------------------------------------------- |:--------:|
| userID?  | integer | the ID of the user                                             |    false    |
| size?    | integer | the size of the image                                          |    false    |
| dynamic? | string  | dynamic image <br /> 1. **true** (default) <br /> 2. **false** |    false    |
| format?  | string  |                                                                |    false    |


## Example

This will return your profile picture:

```javascript
bot.command({
  name: 'userAvatar',
  code: `
  $userAvatar[$authorID;2048;true;webp]
  `
});
```

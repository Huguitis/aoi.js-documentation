---
title: $userBanner 
description: $userBanner will return the profile banner of a specific user.
id: userBanner
---

`$userBanner` will return the profile banner of a specific user.

## Usage

```php
$userBanner[userID?;size?;dynamic?;format?]
```

## Parameters 


| Field    | Type    | Description                                                    | Required |
| -------- | ------- | -------------------------------------------------------------- |:--------:|
| userID?  | integer | the ID of the user                                             |    no    |
| size?    | integer | the size of the image                                          |    no    |
| dynamic? | string  | dynamic image <br /> 1. **true** (default) <br /> 2. **false** |    no    |
| format?  | string  |                                                                |    no    |


## Example

This will return your profile banner:

```javascript
bot.command({
  name: 'userBanner',
  code: `
  $userBanner[$authorID;4096;true;webp]
  `
});
```

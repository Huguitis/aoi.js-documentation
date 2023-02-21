---
title: $usersInChannel 
description: $usersInChannel will return all users who are connected to the specified voice channel.
id: usersInChannel
---

`$usersInChannel` will return all users who are connected to the specified voice channel.

## Usage

```php
$usersInChannel[channelID;option?;sep?]
```

## Parameters 


| Field     | Type    | Description                                                                                | Required |
| --------- | ------- | ------------------------------------------------------------------------------------------ |:--------:|
| channelID | integer | voice channel ID                                                                           |    true   |
| option?   | string  | how to return the users <br /> 1. **id** (default) <br /> 2. **user** - mentions the users |    false    |
| sep?      | string  | seperator                                                                                  |    false    |


## Example

This will return the users connected to a voice channel:

##### Make sure you're in a voice channel when using this example or else it will not work.


```javascript
bot.command({
  name: 'usersInChannel',
  code: `
  $usersInChannel[$voiceID;user;, ]
  `
});
```

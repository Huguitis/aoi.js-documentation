---
title: $channelID 
description: $channelID will return the channel ID of the given channel name.
id: channelID
---

`$channelID` will return the channel ID of the given channel name.

## Usage

```php
$channelID[name?]
```

## Parameters 


| Field | Type    | Description                                            | Required |
| ----- | ------- | ------------------------------------------------------ | -------- |
| name? | integer | channel name of the channel you want the channel ID of | no       |


## Example

This will return the channel ID of the channel where you're executing the command:

```javascript
bot.command({
  name: 'channelID',
  code: `
  $channelID
  `
});
```
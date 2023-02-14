---
title: $fetchActiveThreads 
description: $fetchActiveThreads will return all active threads of a given channel.
id: fetchActiveThreads
---

`$fetchActiveThreads` will return all active threads of a given channel.

## Usage

```php
$fetchActiveThreads[channelID;option?]
```

## Parameters 


| Field     | Type    | Description                                                                    | Required |
| --------- | ------- | ------------------------------------------------------------------------------ |:--------:|
| channelID | integer | channel ID                                                                     |    yes   |
| option?   | string  | how to return the active threads <br /> 1. **name** (default) <br /> 2. **id** |    no    |

## Example

This will return all active threads, if any:

```javascript
bot.command({
  name: 'fetchActiveThreads',
  code: `
  $fetchActiveThreads[$channelID;name]
  `
});
```
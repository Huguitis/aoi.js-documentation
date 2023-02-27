---
title: $fetchArchivedThreads
description: $fetchArchivedThreads will return all archived threads of a given channel.
id: fetchArchivedThreads
---

`$fetchArchivedThreads` will return all archived threads of a given channel.

## Usage

```php
$fetchArchivedThreads[channelID;option?]
```

## Parameters

| Field     | Type    | Description                                                                    | Required |
|-----------|---------|--------------------------------------------------------------------------------|:--------:|
| channelID | integer | channel ID                                                                     |   true   |
| option?   | string  | how to return the active threads <br /> 1. **name** (default) <br /> 2. **id** |  false   |

## Example

This will return all archived threads, if any:

```javascript
bot.command({
    name: 'fetchArchivedThreads',
    code: `
  $fetchArchivedThreads[$channelID;name]
  `
});
```
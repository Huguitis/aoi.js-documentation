---
title: $deleteStageInstance 
description: $deleteStageInstance will delete an existing stage instance.
id: deleteStageInstance
---

`$deleteStageInstance` will delete an existing stage instance.

## Usage

```php
$deleteStageInstance[channelID]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| channelID    | integer  | channel ID                             | yes      |


## Example

This will end the current stage instance: ( make sure to replace stageID with an actual stage ID )

```javascript
bot.command({
  name: 'deleteStageInstance',
  code: `
  $deleteStageInstance[stageInstance]
  `
});
```
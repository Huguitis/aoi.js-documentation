---
title: $createStageInstance 
description: $createStageInstance will start a stage.
id: createStageInstance
---

`$createStageInstance` will start a stage.

## Usage

```php
$createStageInstance[channelID;topic;type?]
```

## Parameters 


| Field     | Type    | Description    | Required |
| --------- | ------- | -------------- |:--------:|
| channelID | integer | stage voice ID |    true   |
| topic     | string  | stage topic    |    true   |
| type?     | string  | stage type     |    false    |

<details>
  <summary><h3> Invite Target Types </h3></summary>

| TYPE    | VALUE |
| ------- | ----- |
| PUBLIC  | 1     |
| PRIVATE | 2     |

</details>

## Examples

This will create start a stage:

```javascript
bot.command({
  name: 'createStageInstance',
  code: `
  $createStageInstance[stageID;Testing!;1] // replace "stageID" with an actual stage ID
  `
});
```

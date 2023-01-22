---
title: $interactionFollowUp 
description: $interactionFollowUp can be used for JSON requests, song informations or playing tracks, since these things takes more than 3 seconds.

id: interactionFollowUp
---

`$interactionFollowUp` can be used for JSON requests, song informations or playing tracks, since these things takes more than 3 seconds.

## Usage

```php
$interactionFollowUp[content?;embeds?;components?;files?;ephemeral ?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| content?    | string  | message content                             | no      |
| embeds?    | string  | embed                             | no      |
| components?    | string  | components                             | no      |
| files?    | string  | files                             | no      |
| ephemeral ?    | string  | visible to the command author only? <br> 1. **yes** <br> 2. **no** (default)                             | no      |


## Example

```javascript
bot.interactionCommand({
  name: "interactionFollowUp",
  prototype: 'slash',
  code: `
  $interactionFollowUp[Bye, world!]
  $interactionDefer[yes]
  `
});
```

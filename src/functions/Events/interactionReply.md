---
title: $interactionReply 
description: $interactionReply allows you to send an interaction message reply.

id: interactionReply
---

`$interactionReply` allows you to send an interaction message reply.

## Usage

```php
$interactionReply[content?;embeds?;components?;files?;allowedMention?s;ephemeral?]
```

## Parameters 


| Field            | Type   | Description                                                                                       | Required |
| ---------------- | ------ | ------------------------------------------------------------------------------------------------- |:--------:|
| content?         | string | message content                                                                                   |    no    |
| embeds?          | string | embed                                                                                             |    no    |
| components?      | string | components                                                                                        |    no    |
| files?           | string | files                                                                                             |    no    |
| allowed mentions | string | what can be mentioned in the reply <br /> 1. **everyone** <br /> 2. **roles** <br /> 3. **users** |    no    |
| ephemeral?       | string | visible to the command author only? <br /> 1. **true** <br /> 2. **false** (default)              |    no    |


## Example

```javascript
bot.interactionCommand({
  name: "interactionReply",
  prototype: 'slash',
  code: `
  $interactionReply[Hello, world!;;;;everyone;false]
  `
});
```

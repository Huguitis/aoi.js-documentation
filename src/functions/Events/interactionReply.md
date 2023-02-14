---
title: $interactionReply 
description: $interactionReply allows you to send an interaction message reply.

id: interactionReply
---

`$interactionReply` allows you to send an interaction message reply.

## Usage

```php
$interactionReply[content?;embeds?;components?;files?;allowedMentions?;ephemeral?]
```

## Parameters 


| Field            | Type   | Description                                                                                       | Required |
| ---------------- | ------ | ------------------------------------------------------------------------------------------------- |:--------:|
| content?         | string | message content                                                                                   |    false    |
| embeds?          | string | embed                                                                                             |    false    |
| components?      | string | components                                                                                        |    false    |
| files?           | string | files                                                                                             |    false    |
| allowedMentions? | string | what can be mentioned in the reply <br /> 1. **everyone** <br /> 2. **roles** <br /> 3. **users** |    false    |
| ephemeral?       | string | visible to the command author only? <br /> 1. **true** <br /> 2. **false** (default)              |    false    |


## Example

```javascript
bot.interactionCommand({
  name: "interactionReply",
  prototype: "slash", // button/selectMenu/slash
  code: `
  $interactionReply[Hello, world!;;;;everyone;false]
  `
});
```

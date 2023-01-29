---
title: $interactionEdit 
description: $interactionEdit will return edit an interaction.
id: interactionEdit
---

`$interactionEdit` will return edit an interaction.

## Usage

```php
$interactionEdit[content?;embeds?;components?;files?;allowedMentions?]
```

## Parameters 


| Field           | Type   | Description                                                                     | Required |
| --------------- | ------ | ------------------------------------------------------------------------------- |:--------:|
| content?        | string | message content                                                                 |    no    |
| embeds?         | string | embed                                                                           |    no    |
| components?     | string | components                                                                      |    no    |
| files?          | string | files                                                                           |    no    |
| allowedMentions | string | allowed mentions <br /> 1. **users** <br /> 2. **roles** <br /> 3. **everyone** |    no    |


## Example

```javascript
bot.interactionCommand({
  name: "interactionEdit",
  prototype: 'slash',
  code: `
  $interactionEdit[Bye, World!;;;;everyone]
  $wait[5s]
  $interactionReply[Hello, World!;;;;everyone;false]
  `
});
```

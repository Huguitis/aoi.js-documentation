---
title: $interactionUpdate 
description: $interactionUpdate will update an existing interaction.
id: interactionUpdate
---

`$interactionUpdate` will return edit an interaction.

## Usage

```php
$interactionUpdate[content?;embeds?;components?;files?]
```

## Parameters 


| Field       | Type   | Description     | Required |
| ----------- | ------ | --------------- |:--------:|
| content?    | string | message content |    no    |
| embeds?     | string | embed           |    no    |
| components? | string | components      |    no    |
| files?      | string | files           |    no    |


## Example

```javascript
bot.interactionCommand({
  name: "interactionUpdate",
  prototype: 'slash',
  code: `
  $interactionUpdate[Bye, World!]
  $wait[5s]
  $interactionReply[Hello, World!;;;;everyone;false]
  `
});
```

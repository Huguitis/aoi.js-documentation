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
| content?    | string | message content |    false    |
| embeds?     | string | embed           |    false    |
| components? | string | components      |    false    |
| files?      | string | files           |    false    |


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

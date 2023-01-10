---
title: $interactionEdit 
description: $interactionEdit will return edit an interaction.
id: interactionEdit
---

`$roleCount` will return edit an interaction.

## Usage

```php
$interactionEdit[content?;embeds?;components?;files?;allowed mentions?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| content?    | string  | message content                             | no      |
| embeds?    | string  | embed                             | no      |
| components?    | string  | components                             | no      |
| files?    | string  | files                             | no      |
| allowed mentions?    | string  | allowed mentions <br> 1. **users** <br> 2. **roles** <br> 3. **everyone**                             | no      |


## Example

```javascript
bot.interactionCommand({
  name: "interactionEdit",
  prototype: 'slash',
  code: `
  $interactionEdit[Bye, World!]
  $wait[5s]
  $interactionReply[Hello, World!]
  `
});
```

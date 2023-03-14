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

| Field            | Type   | Description                                                                     | Required |
|------------------|--------|---------------------------------------------------------------------------------|:--------:|
| content?         | string | message content                                                                 |  false   |
| embeds?          | string | embed                                                                           |  false   |
| components?      | string | components                                                                      |  false   |
| files?           | string | files                                                                           |  false   |
| allowedMentions? | string | allowed mentions <br /> 1. **users** <br /> 2. **roles** <br /> 3. **everyone** |  false   |

## Example

```javascript
bot.interactionCommand({
    name: "interactionEdit",
    prototype: "slash",
    code: `
  $interactionEdit[Bye, World!;;;;everyone]
  $wait[5s]
  $interactionReply[Hello, World!;;;;everyone;false]
  `
});
```

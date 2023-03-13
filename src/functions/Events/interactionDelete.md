---
title: $interactionDelete
description: $interactionDelete will delete a reply of an interaction.
id: interactionDelete
---

`$interactionDelete` will delete a reply of an interaction.

## Usage

```php
$interactionDelete
```

## Example

This will delete the interaction after 5 seconds.

```javascript
bot.interactionCommand({
    name: "interactionEdit",
    prototype: "button",
    code: `
  $interactionDelete
  $wait[5s]
  $interactionReply[Hello, World!;;;;everyone;false]
  `
});
```

---
title: $deleteEmoji 
description: $deleteEmoji will delete a specific emoji.
id: deleteEmoji
---

`$deleteEmoji` will delete a specific emoji.

## Usage

```php
$deleteEmoji[emoji]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| emoji     | string  | emoji name, id or full form                        | yes      |


## Example

This will delete a random emoji of your guild:

```javascript
bot.command({
  name: 'deleteEmoji',
  code: `
  $deleteEmoji[$randomEmoji]
  `
});
```

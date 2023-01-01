---
title: $messageSlice 
description: $messageSlice will slice a message.
id: messageSlice
---

`$messageSlice` will slice a message.

## Usage

```php
$messageSlice[from?;to?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| from?     | number  | starting point where to slice the message          | no       |
| to?        | number  | ending point where slicing ends                    | no      |


## Example

This will slice the message with any given argument:

```javascript
bot.command({
  name: 'messageSlice',
  code: `
  $messageSlide[from?;to?]
  `
});
```

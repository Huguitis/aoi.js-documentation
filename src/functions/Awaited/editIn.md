---
title: $editIn 
description: $editIn will edit a message after a given time.
id: editIn
---

`$editIn` will edit a message after a given time.

## Usage

```php
$editIn[time;content]
```

## Parameters 


| Field   | Type   | Description                                 | Required |
| ------- | ------ | ------------------------------------------- |:--------:|
| time    | string | after how much time the message gets edited |    true   |
| content | string | what the new message should be              |    true   |


## Example

This will edit the sent message after five seconds:

```javascript
bot.command({
  name: 'editIn',
  code: `
  $editIn[5s;aoi.js is great, don't you agree?]
  I'll edit this message in 5 seconds!
  `
});
```

---
title: $description 
description: $description is used for embeds to add an description field.
id: description
---

`$description` is used for embeds to add an description field.

## Usage

```php
$description[index?;description]
```

## Parameters 


| Field       | Type   | Description                        | Required |
| ----------- | ------ | ---------------------------------- |:--------:|
| index?      | number | embed index                        |    false    |
| description | string | content of the embed's description |    true   |


## Example

This will send an embed with the content `aoi.js is great!`:

```javascript
bot.command({
  name: 'embed',
  code: `
  $description[aoi.js is great!]
  `
});
```
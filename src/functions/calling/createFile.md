---
title: $createFile 
description: $createFile will create a file.
id: createFile
---

`$createFile` will create a file.

## Usage

```php
$createFile[attachment;name]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| attachment    | string  | content of the file                 | yes      |
| name    | string  | name of the file                             | yes      |


## Example

This will create a text file called **`example.txt`** with the text "This is an example!":

```javascript
bot.command({
  name: 'createFile',
  code: `
  $createFile[This is an example!;example.txt]
  `
});
```

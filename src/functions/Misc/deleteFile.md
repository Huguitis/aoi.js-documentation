---
title: $deleteFile
description: $deleteFile will delete a given file of your directory.
id: deleteFile
---

`$deleteFile` will delete a given file of your directory.

## Usage

```php
$deleteFile[path]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| path    | string   | file path                                                         |   true   |

## Example

This will delete your `index.js` (don't actually do that):

```javascript
bot.command({
    name: "deleteFile",
    code: `
  $deleteFile[./index.js]
  `
});
```
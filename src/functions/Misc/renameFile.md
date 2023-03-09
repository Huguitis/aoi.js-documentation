---
title: $renameFile
description: $renameFile will rename a file of your bot's directory.
id: renameFile
---

`$renameFile` will rename a file of your bot's directory.

## Usage

```php
$renameFile[oldFile;newFile]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| oldFile    | string   | old file name                                                         |   true   |
| newFile    | string   | new file name                                                         |   true   |

## Example

This will change your index.js to a index.txt file:

```javascript
bot.command({
    name: "renameFile",
    code: `
    $renameFile[./index.js;./index.txt]
    `
});
```
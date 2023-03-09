---
title: $onlyNSFW
description: $onlyNSFW will check if the command was executed in a NSFW channel and return a error message if not.
id: onlyNSFW
---

`$onlyNSFW` will check if the command was executed in a NSFW channel and return a error message if not.

## Usage

```php
$onlyNSFW[error?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| error?    | string   | error to return when the command was not executed in a NSFW channel  |   false   |

## Examples

This will limit the command only to NSFW channels:

```javascript
bot.command({
    name: "onlyNSFW",
    code: `
    $onlyNSFW[You can't use that command here!]
    `
});
```
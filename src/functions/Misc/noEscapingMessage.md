---
title: $noEscapingMessage
description: $noEscapingMessage will return the non escaped message.
id: noEscapingMessage
---

`$noEscapingMessage` will return the non escaped message.

## Usage

```php
$noEscapingMessage[args]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| args?    | string   | message position                                                    |   false   |

## Examples

```javascript
bot.command({
    name: "noEscapingMessage",
    code: `
    $noEscapingMessage[1]
    `
});
```
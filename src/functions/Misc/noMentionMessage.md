---
title: $noMentionMessage
description: $noMentionMessage will return the part of the message which contains no mention.
id: noMentionMessage
---

`$noMentionMessage` will return the part of the message which contains no mention.

## Usage

```php
$noMentionMessage[args]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| args?    | string   | message position                                                    |   fals   |

## Examples

```javascript
bot.command({
    name: "noMentionMessage",
    code: `
    $noMentionMessage[1]
    `
});
```
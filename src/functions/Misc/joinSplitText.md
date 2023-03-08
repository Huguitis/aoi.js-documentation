---
title: $joinSplitText
description: $joinSplitText will join all text split elements by a given seperator.
id: joinSplitText
---

`$joinSplitText` will join all text split elements by a given seperator.

## Usage

```php
$joinSplitText[sep?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| sep?    | integer   | seperator                         |   false   |

## Example

This will join all text split elements with a comma:

```javascript
bot.command({
    name: "joinSplitText",
    code: `
    $joinSplitText[, ]
    $textSplit[Hello:Bye:Leref;:]
    `
});
```
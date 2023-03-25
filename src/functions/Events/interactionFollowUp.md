---
title: $interactionFollowUp
description: $interactionFollowUp can be used for JSON requests, song information or playing tracks, since these things
takes more than 3 seconds.
id: interactionFollowUp
---

`$interactionFollowUp` can be used for JSON requests, song information or playing tracks, since these things takes more
than 3 seconds.

## Usage

```php
$interactionFollowUp[content?;embeds?;components?;files?;ephemeral?]
```

## Parameters

| Field       | Type   | Description                                                                          | Required |
|-------------|--------|--------------------------------------------------------------------------------------|:--------:|
| content?    | string | message content                                                                      |  false   |
| embeds?     | string | embed                                                                                |  false   |
| components? | string | components                                                                           |  false   |
| files?      | string | files                                                                                |  false   |
| ephemeral?  | string | visible to the command author only? <br /> 1. **true** <br /> 2. **false** (default) |  false   |

## Example

```javascript
bot.interactionCommand({
    name: "interactionFollowUp",
    prototype: "slash",
    code: `
  $interactionFollowUp[Bye, world!]
  $interactionDefer[true]
  `
});
```

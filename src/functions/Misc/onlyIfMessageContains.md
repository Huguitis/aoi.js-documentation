---
title: $onlyIfMessageContains
description: $onlyIfMessageContains will check if the message contains the given text and if not return a error message.
id: onlyIfMessageContains
---

`$onlyIfMessageContains` will check if the message contains the given text and if not return a error message.

## Usage

```php
$onlyIfMessageContains[message;...text;error?]
```

## Parameters

| Field   | Type                    | Description                                 | Required |
|---------|-------------------------|---------------------------------------------|:--------:|
| message | string, integer, number | message which should contain the given text |   true   |
| text    | string, integer, number | text to check for in the message            |   true   |
| error?  | string                  | error to return                             |  false   |

## Example(s)

This will return the error message as "aoi.js" does not appear in "Hello!":

```javascript
bot.command({
    name: "onlyIfMessageContains",
    code: `
    $onlyIfMessageContains[Hello!;aoi.js;Couldn't find that word!]
    `
});
```
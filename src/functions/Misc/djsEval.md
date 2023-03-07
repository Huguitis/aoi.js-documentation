---
title: $djsEval
description: $djsEval will execute given discord.js code.
id: djsEval
---

`$djsEval` will execute given discord.js code.

## Usage

```php
$djsEval[code;returnCode?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| code    | string   | discord.js code                                                         |   true   |
| returnCode?    | string   | return code <br /> 1. **true** <br /> 2. **false** (default)     |   false   |

## Example

This will return your user ID:

```javascript
bot.command({
    name: "djsEval",
    code: `
  $djsEval[msg.author.id;true]
  `
});
```
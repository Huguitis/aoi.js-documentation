---
title: $exec
description: $exec will execute given code in your console.
id: exec
---

`$exec` will execute given code in your console.

## Usage

```php
$exec[code]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| code      | string   | code to execute in your console                                    |   true   |

## Example

This will return your node version:

```javascript
bot.command({
    name: "exec",
    code: `
    \`\`\`
    $exec[node -v]
    \`\`\`
  `
});
```
---
title: $mentionedRolesCount 
description: $mentionedRolesCount will return the amount of role mentions within a message.
id: mentionedRolesCount
---

`$mentionedRolesCount` will return the amount of role mentions within a message.

## Usage

```php
$mentionedRolesCount
```

## Example

This will return the amount of role mentions in the given text:

```javascript
bot.command({
  name: 'mentionedRolesCount',
  code: `
  $mentionedRolesCount
  <@&1008551437686546483> <@&1058540613173260449>
`
});
```

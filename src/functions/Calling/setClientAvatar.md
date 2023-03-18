---
title: $setClientAvatar
description: $setClientAvatar will change the clients' avatar.
id: setClientAvatar
---

`$setClientAvatar` will change the clients' avatar.

## Usage

```php
$setClientAvatar[avatar]
```

## Parameters

| Field  | Type   | Description    | Required |
|--------|--------|----------------|:--------:|
| avatar | string | new avatar URL |   true   |

## Example

This will change the client's avatar to the command author's user avatar:

```javascript
bot.command({
    name: 'setClientAvatar',
    code: `
   $setClientAvatar[$userAvatar[$authorID]]`
});
```
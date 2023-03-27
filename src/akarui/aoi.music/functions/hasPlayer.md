---
title: $hasPlayer
description: $hasPlayer will return either true or false depending on if the current instance has a player.
id: hasPlayer
---

`$hasPlayer` will return either true or false depending on if the current instance has a player.

## Usage

```php
$hasPlayer
```

## Example

This will return either true or false depending on if your bot has a player or not:

```javascript
bot.command({
    name: 'hasPlayer',
    code: `
    $hasPlayer
  `
});
```
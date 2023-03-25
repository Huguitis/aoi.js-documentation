---
title: $isValidInvite
description: $isValidInvite will check if the given invite is valid.
id: isValidInvite
---

`$isValidInvite` will check if the given invite is valid.

## Usage

```php
$isValidInvite[URL]
```

## Parameters

| Field | Type   | Description      | Required |
|-------|--------|------------------|----------|
| URL   | string | guild invite URL | true     |

## Example

This will return `true` as `https://discord.gg/aoi-js-server-akarui-development-team-773352845738115102` is an valid
invite:

```javascript
bot.command({
    name: 'isValidInvite',
    code: `
  $isValidInvite[https://discord.gg/aoi-js-server-akarui-development-team-773352845738115102]
  `
});
```

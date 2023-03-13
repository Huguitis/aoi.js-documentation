---
title: $closeTicket
description: $closeTicket will delete a ticket created by `$newTicket`.
id: closeTicket
---

`$closeTicket` will delete a ticket created by `$newTicket`.

## Usage

```php
$closeTicket[error?]
```

## Parameters

| Field  | Type   | Description     | Required |
|--------|--------|-----------------|:--------:|
| error? | string | error to return |  false   |

## Example

```javascript
bot.command({
    name: "closeTicket",
    code: `
  $closeTicket[Something went wrong!]
  `
});
```
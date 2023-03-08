---
title: $isTicket
description: $isTicket will return either true or false depending on the channel being a ticket channel.
id: isTicket
---

`$isTicket` will return either true or false depending on the channel being a ticket channel.

## Usage

```php
$isTicket[channelID?]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| channelID?    | integer   | channel ID                         |   false   |

#### Valid Mathematical Operators

| Operator | Mathematical Expression  |
|----------|--------------------------|
| ==       | equal to                 |
| !=       | not equal to             |
| <=       | less than or equal to    |
| \>=      | greater than or equal to |
| \>       | greater than             |
| <        | less than                |
| \|\|     | logical OR               |
| &&       | logical conjunction      |

## Example

This will check if the current channel is a ticket channel created by `$newTicket`:

```javascript
bot.command({
    name: "isTicket",
    code: `
    $isTicket[$channelID]
    `
});
```
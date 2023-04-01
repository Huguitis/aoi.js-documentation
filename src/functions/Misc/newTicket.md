---
title: $newTicket
description: $newTicket will create a new ticket channel.
id: newTicket
---

`$newTicket` will create a new ticket channel.

## Usage

```php
$newTicket[name;msg;categoryID?;returnId?;error?]
```

## Parameters

| Field       | Type    | Description                                                            | Required |
|-------------|---------|------------------------------------------------------------------------|:--------:|
| name        | string  | channel name                                                           |   true   |
| msg         | string  | start message                                                          |   true   |
| categoryID? | integer | where to place the channel after creation                              |  false   |
| returnId?   | string  | return the channel ID <br /> 1. **true** <br /> 2. **false** (default) |  false   |
| error?      | string  | error to return when something went wrong                              |  false   |

## Example(s)

This will create a new ticket:

```javascript
bot.command({
    name: "newTicket",
    code: `
    $newTicket[ticket-$username;Hello <@$authorID!;$guildID;false;Error!]
    `
});
```

This will create a new ticket and send an embed:

```javascript
bot.command({
    name: "newTicket",
    code: `
    $newTicket[ticket-$username;Hello <@$authorID! {newEmbed:{description:<@$authorID> opened a new ticket!}};$guildID;false;Error!]
    `
});
```
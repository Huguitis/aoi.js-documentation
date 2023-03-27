---
title: $queue
description: $queue will return the current song queue.
id: queue
---

`$queue` will will return the current song queue.

## Usage

```php
$queue[page?;limit?;format?]
```

## Parameters

| Field   | Type   | Description                                   | Required |
|---------|--------|-----------------------------------------------|:--------:|
| page?   | number | queue page                                    |  false   |
| limit?  | number | maximum of songs to display                   |  false   |
| format? | string | format to display information about the songs |  false   |

<details open>
  <summary><h3> Format </h3></summary>

|                                              | Format                           |
|----------------------------------------------|----------------------------------|
| Song Title                                   | `{title}`                        |
| Song Position                                | `{position}`                     |
| Song Duration                                | `{duration}`                     |
| Song Requester (user ID)                     | `{requester.user.id}`            |
| Song Requester (username)                    | `{requester.user.name}`          |
| Song Requester (username with discriminator) | `{requester.user.tag}`           |
| Song Requester (discriminator)               | `{requester.user.discriminator}` |
| Song Requester (mention)                     | `{requester.user.mention}`       |

</details>

## Example

This will return the current queue in the `{position}) {title} - {requester.user.name}` format:

```javascript
bot.command({
    name: 'queue',
    code: `
    $queue[1;10;{position}) {title} - {requester.user.name}]
  `
});
```
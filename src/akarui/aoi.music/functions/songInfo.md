---
title: $songInfo
description: $songInfo will return given song's information.
id: songInfo
---

`$songInfo` will will return given song's information.

## Usage

```php
$songInfo[type?;position?]
```

## Parameters

| Field     | Type   | Description             | Required |
|-----------|--------|-------------------------|:--------:|
| type?     | string | information to retrieve |  false   |
| position? | number | track position          |  false   |

<details open>
  <summary><h3> Format </h3></summary>

|                                              | Format               |
|----------------------------------------------|----------------------|
| Song Title                                   | `title`              |
| Song URL                                     | `url`                |
| Song Author                                  | `author`             |
| Song Author                                  | `authorURL`          |
| Song Position                                | `position`           |
| Song Duration                                | `duration`           |
| Song Requester (user ID)                     | `user.id`            |
| Song Requester (username)                    | `user.name`          |
| Song Requester (username with discriminator) | `user.tag`           |
| Song Requester (discriminator)               | `user.discriminator` |
| Song Requester (mention)                     | `user.mention`       |

</details>

## Example

This will return the current track name:

```javascript
bot.command({
    name: 'songInfo',
    code: `
    $songInfo[title]
  `
});
```
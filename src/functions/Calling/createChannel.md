---
title: $createChannel
description: $createChannel will create a channel of a given type.
id: createChannel
---

`$createChannel` will create a channel of a given type.

## Usage

```php
$createChannel[guildID;name;type;returnID;parentID]
```

## Parameters

| Field    | Type    | Description                                                        | Required |
|----------|---------|--------------------------------------------------------------------|:--------:|
| guildID  | integer | guild id                                                           |   true   |
| name     | string  | channel name                                                       |   true   |
| type     | string  | channel type                                                       |   true   |
| returnID | boolean | return channel ID <br /> 1. **true** <br /> 2. **false** (default) |   true   |
| parentID | integer | category ID                                                        |  false   |

<details open>
  <summary><h3> Channel Types </h3></summary>

| Channel Type         |                    |
|----------------------|--------------------|
| Text Channel         | Text               |
| Voice Channel        | Voice              |
| Category             | Category           |
| Stage Channel        | Stage              |
| Private Thread       | PrivateThread      |
| Public Thread        | PublicThread       |
| Forum                | Forum              |
| Announcement Thread  | AnnouncementThread |
| Announcement Channel | Announcement       |

</details>

## Example(s)

This will create a new text channel called "aoi.js":

```javascript
bot.command({
    name: 'createChannel',
    code: `
    $createChannel[$guildID;aoi.js;Text;false]
  `
});
```

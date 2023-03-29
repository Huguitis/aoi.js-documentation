---
title: $editChannel
description: $editChannel will edit a channel.
id: editChannel
---

`$editChannel` will edit a channel.

## Usage

```php
$editChannel[channelID;name?;type?;position?;topic?;nsfw?;bitrate?;userlimit?;parent?;lockPermissions?;permissionOverwrites?;rateLimitPerUser?;defaultAutoArchiveDuration?;rtcRegion?;reason?]
```

## Parameters

| Field                       | Type    | Description                                             | Required |
|-----------------------------|---------|---------------------------------------------------------|:--------:|
| channelID                   | integer | channel ID                                              |   true   |
| name?                       | string  | new channel name                                        |  false   |
| type?                       | string  | channel type                                            |  false   |
| position?                   | string  | channel position                                        |  false   |
| topic?                      | string  | channel topic                                           |  false   |
| nsfw?                       | string  | mark channel as nsfw                                    |  false   |
| bitrate?                    | integer | voice channel bitrate                                   |  false   |
| userlimit?                  | number  | voice channel userlimit                                 |  false   |
| parent?                     | integer | channel parent (Category)                               |  false   |
| lockPermissions?            | string  | channels lock permissions                               |  false   |
| permissionOverwrites?       | string  | channels overwrites                                     |  false   |
| rateLimitPerUser?           | number  | channel slowmode                                        |  false   |
| defaultAutoArchiveDuration? | number  | thread/forum archive duration (in ms)                   |  false   |
| rtcRegion?                  | string  | voice channel rtc region                                |  false   |
| reason?                     | string  | reason that will be displayed in the guild's audit logs |  false   |

### Note: you can use `$default` to keep the current property.

<details>
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

#### Note: all channel types are **case-sensitive**.

</details>

## Example(s)

This will change the current channel name to "I love aoi.js" and move it to the top:

```javascript
bot.command({
    name: 'editChannel',
    code: `
  $editChannel[$channelID;I love aoi.js;$default;1]
  `
});
```
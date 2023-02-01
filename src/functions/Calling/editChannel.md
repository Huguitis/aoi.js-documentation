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
| --------------------------- | ------- | ------------------------------------------------------- |:--------:|
| channelID                   | integer | channel ID                                              |    yes   |
| name?                       | string  | new channel name                                        |    no    |
| type?                       | string  | channel type                                            |    no    |
| position?                   | string  | channel position                                        |    no    |
| topic?                      | string  | channel topic                                           |    no    |
| nsfw?                       | string  | mark channel as nsfw                                    |    no    |
| bitrate?                    | integer | voice channel bitrate                                   |    no    |
| userlimit?                  | number  | voice channel userlimit                                 |    no    |
| parent?                     | integer | channel parent (Category)                               |    no    |
| lockPermissions?            | string  | channels lock permissions                               |    no    |
| permissionOverwrites?       | string  | channels overwrites                                     |    no    |
| rateLimitPerUser?           | number  | channel slowmode                                        |    no    |
| defaultAutoArchiveDuration? | number  | thread/forum archive duration (in ms)                   |    no    |
| rtcRegion?                  | string  | voice channel rtc region                                |    no    |
| reason?                     | string  | reason that will be displayed in the guild's audit logs |    no    |

### Note: you can use `$default` to keep the current property.

<details>
  <summary><h3> Channel Types </h3></summary>

| Channel Type         |                    |
| -------------------- | ------------------ |
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

## Example

This will change the current channel name to "I love aoi.js" and move it to the top:

```javascript
bot.command({
  name: 'editChannel',
  code: `
  $editChannel[$channelID;I love aoi.js;$default;1]
  `
});
```
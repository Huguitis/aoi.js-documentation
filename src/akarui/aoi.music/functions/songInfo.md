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

<details>
  <summary><h3> Types </h3></summary>

| Property          |                                                        | Returns | Supports                                     |
|-------------------|--------------------------------------------------------|---------|----------------------------------------------|
| title             | Title                                                  | string  | YouTube, Spotify, SoundCloud, Url, LocalFile |
| channelId         | Channel ID                                             | string  | YouTube                                      |
| artist            | Artist                                                 | string  | YouTube, Spotify, SoundCloud                 |
| artistURL         | Artist URL                                             | string  | YouTube, SoundCloud                          |
| artistAvatar      | Artist Avatar                                          | string  | SoundCloud                                   |
| duration          | Duration in ms                                         | number  | YouTube, Spotify, SoundCloud, Url, LocalFile |
| identifier        | soundcloud, youtube, localfile, url, spotify           | string  | YouTube, Spotify, SoundCloud, Url, LocalFile |
| views             | Views/Plays                                            | string  | YouTube, Spotify, SoundCloud, Url, LocalFile |
| likes             | Likes                                                  | number  | YouTube, Spotify, SoundCloud, Url, LocalFile |
| thumbnail         | Thumbnail                                              | number  | YouTube, Spotify, SoundCloud                 |
| id                | ID                                                     | string  | YouTube, Spotify, SoundCloud, Url, LocalFile |
| description       | Description                                            | string  | YouTube, Spotify, SoundCloud                 |
| createdAt         | Creation Date                                          | string  | YouTube, Spotify, SoundCloud                 |
| platformType      |                                                        | string  | YouTube, Spotify, SoundCloud, Url, LocalFile |
| rawData           |                                                        | object  | YouTube, Spotify, SoundCloud, Url, LocalFile |
| formatedPlatforms | SoundCloud, YouTube, Localfile, Url, Spotify           | string  | YouTube, Spotify, SoundCloud, Url, LocalFile |
| requester         | Song Requester (user object, .user.id, .user.name etc) | string  | YouTube, Spotify, SoundCloud, Url, LocalFile |
| position          | Song Position in the current Queue                     | number  | YouTube, Spotify, SoundCloud, Url, LocalFile |

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
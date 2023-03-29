---
title: $addFilter
description: $addFilter will add given filters.
id: addFilter
---

`$addFilter` will add given filters.

## Usage

```php
$addFilter[filter]
```

## Parameters

| Field  | Type   | Description | Required |
|--------|--------|-------------|:--------:|
| filter | string | JSON format |   true   |

| Filter       | Contains                                   | JSON Format                 |
|--------------|--------------------------------------------|-----------------------------|
| NIGHT_CORE   | aresample, asetrate                        | `{"NIGHT_CORE": "value"}`   |
| BASS_BOOST   | bass                                       | `{"BASS_BOOST": "value"}`   |
| 8_D          | extrastereo, aecho, apulsator, stereowiden | `{"8_D": "value"}`          |
| PITCH        | asetrate, atempo, aresample                | `{"PITCH": "value"}`        |
| KAROAKE      | stereotools                                | `{"KAROAKE": "value"}`      |
| SLOWED       | asetrate, aresample                        | `{"SLOWED": "value"}`       |
| DEEP         | asetrate, atempo, aresample                | `{"DEEP": "value"}`         |
| TREBLE_BOOST | treble                                     | `{"TREBLE_BOOST": "value"}` |
| GATE         | agate                                      | `{"GATE": "value"}`         |
| VIBRATO      | vibrato                                    | `{"VIBRATO": "value"}`      |
| FLANGER      | flanger                                    | `{"FLANGER": "value"}`      |
| PHASER       | aphaser                                    | `{"PHASER": "value"}`       |

aoi.music also supports `ffmpeg` built-in filters in json format.

## Example(s)

This will add `NIGHT_CORE` and `BASS_BOOST` filters:

```javascript
bot.command({
    name: 'addFilter',
    code: `
    $addFilter[{"NIGHT_CORE": "1", "BASS_BOOST": "0.3"}]
  `
});
```
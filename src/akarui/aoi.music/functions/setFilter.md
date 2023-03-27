---
title: $setFilter
description: $setFilter will set given filters.
id: setFilter
---

`$setFilter` will set given filters.

## Usage

```php
$setFilter[filter]
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

## Example

This will set the filter to `NIGHT_CORE` and `BASS_BOOST` filters:

```javascript
bot.command({
    name: 'setFilter',
    code: `
    $setFilter[{"NIGHT_CORE": "1", "BASS_BOOST": "0.3"}]
  `
});
```
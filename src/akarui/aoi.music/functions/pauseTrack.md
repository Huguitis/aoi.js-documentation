---
title: $pauseTrack
description: $pauseTrack will pause the current track. 
id: pauseTrack
---

`$pauseTrack` will pause the current track.  

## Usage

```php
$pauseTrack
```

## Example

This will pause the current track:

```javascript
bot.command({
    name: 'pauseTrack',
    code: `
    $pauseTrack
  `
});
```
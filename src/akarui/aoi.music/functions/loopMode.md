---
title: $loopMode
description: $loopMode will 
id: loopMode
---

`$loopMode` will

## Usage

```php
$loopMode[mode?]
```

## Parameters

| Field | Type   | Description                                                                   | Required |
|-------|--------|-------------------------------------------------------------------------------|:--------:|
| mode? | string | loop mode <br /> 1. **queue** (default) <br /> 2. **song** <br /> 3. **none** |  false   |

## Example

This will set the loop mode to the current track:

```javascript
bot.command({
    name: 'loopMode',
    code: `
    $loopMode[song]
  `
});
```
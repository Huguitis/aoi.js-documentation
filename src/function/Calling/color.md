---
title: $color 
description: $color will add color to an embed.
id: color
---

`$color` will add color to an embed

## Usage

```php
$roleCount[index?;hex]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| index?    | integer  | embed index                             | yes      |
| hex    | string  | hex color                             | no      |

<details>
  <summary><h3> Embed Colors </h3></summary>
  
```js
+ Default
+ White
+ Aqua
+ Green
+ Blue
+ Yellow
+ Purple
+ LuminousVividPink
+ Fuchsia
+ Gold
+ Orange
+ Red
+ Grey
+ Navy
+ DarkAqua
+ DarkGreen
+ DarkBlue
+ DarkPurple
+ DarkVividPink
+ DarkGold
+ DarkOrange
+ DarkRed
+ DarkGrey
+ DarkerGrey
+ LightGrey
+ DarkNavy
+ Blurple
+ Greyple
+ DarkButNotBlack
+ NotQuiteBlack
+ Random
```
  
</details>
  
## Example

This will return an red embed:

```javascript
bot.command({
  name: 'color',
  code: `
  $description[What a nice color!]
  $color[Red]
  `
});
```

---
title: $fetch 
description: $fetch will fetch information about a given method using Discord API.
id: fetch
---

`$fetch` will fetch information about a given method using Discord API.

## Usage

```php
$fetch[method;query;...query]
```
## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| method    | string  | method (listed below)                              | yes      |
| query     | string  | input for the method                               | yes      |


<details>
  <summary><h2> Methods </h2></summary>

| Method     |                                     
|------------|
| message    |
| channel    |
| user       |
| invite     |
| webhook    |
| application |
| command    |
| guildPreview |
| guildTemplate |
| premiumStickerPacks |
| sticker     |
| guildCommand|
| default     |

</details>


## Example

This will display information about the message using the `fetch` function:

```javascript
bot.command({
  name: 'fetch',
  code: `
  \`\`\`
  $fetch[message;$messageID]
  \`\`\`
  ` 
});
```

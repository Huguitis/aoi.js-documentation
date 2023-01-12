---
title: $addButton 
description: $addButton will add a button to the bot's message.
id: addButton
---

## Usage

```php
$addButton[index;label;style;customID;disabled?;emoji?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| index       | number  | in which row the button appears                    | yes      |
| label       | string  | the text that will be displayed on the button                                          | yes      |
| style       | string  | the button **[style][dp]**                 | yes      |
| customID       | string  | button custom ID                                          | yes      |
| disabled?       | string  | disabled? <br> 1. **yes** <br> 2. **no** (default)                                          | no      |
| emoji?       | string  | emoji                                          | no      |

<details open>
  <summary><h3> Button Types </h3></summary>

| Name      | Value | Color                    |
| --------- | ----- | ------------------------ |
| Primary   | 1     | blurple                  |
| Secondary | 2     | grey                     |
| Success   | 3     | green                    |
| Danger    | 4     | red                      |
| Link      | 5     | grey, navigates to a URL |
  
</details>


## Example

This adds a primary and link button to the bot's message:

```javascript
bot.command({
  name: 'addButton',
  code: `
Hello!
$addButton[1;Example Button!;primary;exampleButton;no;💔]
$addButton[1;Example Button!;link;https://discord.gg;no]
  `
});
```


[dp]: https://discord.com/developers/docs/interactions/message-components#button-object-button-styles

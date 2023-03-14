---
title: Discord IDs
description: This page is covering all about IDs.
id: copyingids
---

**This page is about emoji, role, user, channel IDs what they do and how to use them inside of code..**

---

There are multiple ways of retrieving emoji IDs, the easiest way would be

`\:emoji:` which will send the emoji as `<:name:id>`.

Well however, if you don't have the possibility to use animate emojis there are other ways..

1. Using `$customEmoji`, it sends the full emoji just by it's name. 

```php
`$customEmoji[name]`
```

2. Using the Developer Console, complicated but works fine.

First choose the one you want from the emoji panel. 

Then, open the Developer Console by pressing Ctrl-Shift-I and Ctrl-Shift-C. (wont work in the public discord version) 

Next, click on the emoji you chose, and look for a long link starting with "https://cdn.discordapp.com/emojis/" and ending with the emoji's extension (like .gif or .png). 

Copy the numbers between **"emojis/"** and the extension.

### Mentioning Roles, Users and Channels

To mention channels, roles or users in your code you simply follow these formats:

Channels/Categories/Forums:
```php
<#channelID>
```

Users:
```php
<@userID> 
```

```php
<@!userID>
```

Roles: 
```php
<@&roleID>
```
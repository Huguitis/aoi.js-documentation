---
title: $handleError 
description: $handleError will return information about an occured error.
id: handleError
---

`$handleError` will return information about an occured error.

## Usage

```php
$handleError[option]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| option    | string  | what to return <br> 1. **function** - function name <br> 2. **command** - command name <br> 3. **error** - error that occured                            | yes      |


## Example

#### You require `bot.onFunctionError();` in your main file in order to use this function!


```javascript
bot.functionErrorCommand({
channel: "channelID (optional)",
code: `Something went wrong in your "$handleError[command]" command! The function "$handleError[function]" returned the error "$handleError[error]"!`
});
```

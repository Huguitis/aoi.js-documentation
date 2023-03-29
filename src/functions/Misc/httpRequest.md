---
title: $httpRequest
description: $httpRequest either posts to or retrieves data from an API.
id: httpRequest
---

`$httpRequest` either posts to or retrieves data from an API.

## Usage

```php
$httpRequest[URL;method?;body?;property?;error?;headerName:headerValue?]
```

## Parameters

| Field     | Type   | Description                                           | Required |
|-----------|--------|-------------------------------------------------------|:--------:|
| URL       | string | URL you want to get/send data to/from                 |   true   |
| method    | string | method <br /> 1. **GET** (default) <br /> 2. **POST** |   true   |
| body?     | string | content                                               |  false   |
| property? | string | property to return (get method)                       |  false   |
| error?    | string | error to return when request fails                    |  false   |
| ...header | string | headerName, headerValue                               |   true   |

## Example(s)

This will return a random dog fact using the `GET` method:

```javascript
bot.command({
    name: "httpRequest",
    code: `
    $httpRequest[https://some-random-api.ml/facts/dog;GET;;fact;Something went wrong.]
    `
});
```
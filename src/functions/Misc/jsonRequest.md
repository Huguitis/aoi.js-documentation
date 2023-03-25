---
title: $jsonRequest
description: $jsonRequest will send a GET request to a given URL.
id: jsonRequest
---

`$jsonRequest` will send a GET request to a given URL.

## Usage

```php
$jsonRequest[URL;property?;error?;headerName:headerValue?]
```

## Parameters

| Field     | Type   | Description                           | Required |
|-----------|--------|---------------------------------------|:--------:|
| URL       | string | URL you want to get/send data to/from |   true   |
| property? | string | property to return (get method)       |  false   |
| error?    | string | error to return when request fails    |  false   |
| ...header | string | headerName, headerValue               |   true   |

## Example

This will return a random dog fact:

```javascript
bot.command({
    name: "jsonRequest",
    code: `
    $jsonRequest[https://some-random-api.ml/facts/dog;fact;Something went wrong.]
    `
});
```
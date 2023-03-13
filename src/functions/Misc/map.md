---
title: $map
description: $map will execute awaited commands for given elements.
id: map
---

`$map` will execute awaited commands for given elements.

## Usage

```php
$map[text;split;awaits;sep?]
```

## Parameters

| Field  | Type   | Description                | Required |
|--------|--------|----------------------------|:--------:|
| text   | string | text                       |   true   |
| split  | string |                            |   true   |
| awaits | string | Awaited Command to execute |   true   |
| sep?   | string | seperator                  |  false   |
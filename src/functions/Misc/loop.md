---
title: $loop
description: $loop will execute awaited commands a given amount of times.
id: loop
---

`$loop` will execute awaited commands a given amount of times.

## Usage

```php
$loop[time;awaitData;...awaitedCmds]
```

## Parameters

| Field          | Type   | Description                   | Required |
|----------------|--------|-------------------------------|:--------:|
| time           | string | how often to execute the loop |   true   |
| awaitData      | string | Await Data                    |   true   |
| ...awaitedCmds | string | Awaited Commands              |   true   |
---
title: $getApplicationCommandID
description: $getApplicationCommandID will return the ID of a given application command.
id: getApplicationCommandID
---

`$getApplicationCommandID` will return the ID of a given application command.

## Usage

```php
$getApplicationCommandID[name;type?]
```

## Parameters

| Field | Type   | Description                                                                                       | Required |
|-------|--------|---------------------------------------------------------------------------------------------------|:--------:|
| name  | string | query                                                                                             |   true   |
| type? | string | application command type <br /> 1. **global** (default) <br /> 2. **guildID** (specific guild ID) |  false   |
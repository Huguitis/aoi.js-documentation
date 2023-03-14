---
title: $findInCache
description: $findInCache will search for given arguments in your bot's cache.
id: findInCache
---

`$findInCache` will search for given arguments in your bot's cache.

## Usage

```php
$findInCache[type;name;prop;value;findType?;returnValue?]
```

## Parameters

| Field        | Type   | Description                                                                                                                       | Required |
|--------------|--------|-----------------------------------------------------------------------------------------------------------------------------------|:--------:|
| type         | string |                                                                                                                                   |   true   |
| name         | string |                                                                                                                                   |   true   |
| prop         | string | property                                                                                                                          |   true   |
| value        | string | property value                                                                                                                    |   true   |
| findType?    | string | 1. **includes** <br /> 2. **startsWith** <br /> 3. **endsWith** <br /> 4. **>=**, **==**, **===** (default), **<=**, **<**, **>** |  false   |
| returnValue? | string | 1. **$default** (default)                                                                                                         |  false   |
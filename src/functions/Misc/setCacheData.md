---
title: $setCacheData
description: $setCacheData will modify given cache data.
id: setCacheData
---

`$setCacheData` will modify given cache data.

## Usage

```php
$setCacheData[type;cacheName;cacheKey;cacheValue]
```

## Parameters

| Field     | Type     | Description                                                        | Required |
|-----------|----------|--------------------------------------------------------------------|:--------:|
| type    | string   | cache type                                                         |   true   |
| cacheName    | string, integer, number   | cache name                                                         |   true   |
| cacheKey    | string, integer, number   | cache key                                                         |   true   |
| cacheValue    | string, integer, number   | cache value                                                         |   true   |
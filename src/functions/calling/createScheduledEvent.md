---
title: $createScheduledEvent 
description: $createScheduledEvent will create a scheduled event.
id: createScheduledEvent
---

`$roleCount` will create a scheduled event.

## Usage

```php
$roleCount[channelID;name;description;starTime;endTime?;entityType?;entityMetadata?;image?;reason?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| channelID    | integer  | channel ID                             | yes      |
| name    | string  | event name                             | yes      |
| description    | string  | event description                             | yes      |
| starTime    | string  | event start time                             | yes      |
| endTime?    | string  | event end time                             | yes      |
| entityType?    | string  | event type                             | yes      |
| entityMetadata?    | string  | metadata                             | yes      |
| image?    | string  | image                             | yes      |
| reason?    | string  | reason                             | yes      |

---
title: $createScheduledEvent 
description: $createScheduledEvent will create a scheduled event.
id: createScheduledEvent
---

`$createScheduledEvent` will create a scheduled event.

## Usage

```php
$createScheduledEvent[channelID;name;description;starTime;endTime?;entityType?;entityMetadata?;image?;reason?]
```

## Parameters 


| Field           | Type    | Description       | Required |
| --------------- | ------- | ----------------- |:--------:|
| channelID       | integer | channel ID        |    yes   |
| name            | string  | event name        |    yes   |
| description     | string  | event description |    yes   |
| starTime        | string  | event start time  |    yes   |
| endTime?        | string  | event end time    |    no   |
| entityType?     | string  | event type        |    no   |
| entityMetadata? | string  | metadata          |    no   |
| image?          | string  | image             |    no   |
| reason?         | string  | reason            |    no   |

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
| channelID       | integer | channel ID        |    true   |
| name            | string  | event name        |    true   |
| description     | string  | event description |    true   |
| starTime        | string  | event start time  |    true   |
| endTime?        | string  | event end time    |    false   |
| entityType?     | string  | event type        |    false   |
| entityMetadata? | string  | metadata          |    false   |
| image?          | string  | image             |    false   |
| reason?         | string  | reason            |    false   |

---
title: $interactionDefer 
description: $interactionDefer delays messages for the last 15 minutes, which works well for $interactionFollowUp functions.
id: interactionDefer
---

`$interactionDefer` delays messages for the last 15 minutes, which works well for $interactionFollowUp functions.

## Usage

```php
$interactionDefer[ephemeral]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| ephemeral    | integer  | visible to the command author only? yes/no                             | yes      |

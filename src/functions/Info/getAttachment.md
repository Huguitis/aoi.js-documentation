---
title: $getAttachment 
description: $getAttachment will return the properties of an attachment.
id: getAttachment
---

`$getAttachment` will return the properties of an attachment.

## Usage

```php
$getAttachment[channelID;messageID;index?;option?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------| :------: |
| channelID    | integer  | guild ID                           | yes      |
| messageID    | integer  | message ID                           | yes      |
| index?    | number  | attachment index                           | no      |
| option?    | string  | property                           | no      |
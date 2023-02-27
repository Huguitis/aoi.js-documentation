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

| Field     | Type    | Description      | Required |
| --------- | ------- | ---------------- |:--------:|
| channelID | integer | guild ID         |    true   |
| messageID | integer | message ID       |    true   |
| index?    | number  | attachment index |    false    |
| option?   | string  | property         |    false    |
---
title: $parseDate 
description: $parseDate will slide multiple arguments depending on the arguments.
id: parseDate
---

`$parseDate` will slide multiple arguments depending on the arguments.

## Usage

```php
$parseDate[ms;type?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| ms      | string  | text you want to slice                             | yes      |
| type?     | string  | the type in which the parsed Date will be returned in         | no       |

### Types
| Type      | Format    |
|-----------|-----------|
| time        | 1 years, 1 week, 6 days, 8 hours, 16 minutes, 20 seconds    |
| date     | 1/1/2023, 8:16:20 AM    |


## Example

This will return your current date in the `date` [format](/../../util/parseDate.md#types):

```javascript
bot.command({
  name: 'parseDate',
  code: `
  $parseDate[$dateStamp;date]
  `
});
```

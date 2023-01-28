---
title: $editGuild 
description: $editGuild will edit a Discord guild. The function allows you to edit various aspects of the guild.
id: editGuild
---

`$editGuild` will edit a Discord guild. The function allows you to edit various aspects of the guild.

## Usage

```php
$editGuild[guildID;name;verificationLevel?;explicitContentFilter?;afkChannel?;systemChannel?;afkTimeout?;icon?;owner?;splash?;discoverySplash?;banner?;defaultMessageNotifications?;systemChannelFlags?;rulesChannel?;publicUpdatesChannel?;preferredLocale?;description?;features?]
```

## Parameters 


| Field                        | Type    | Description                                                   | Required |
| ---------------------------- | ------- | ------------------------------------------------------------- |:--------:|
| guildID                      | integer | guild ID                                                      |    yes   |
| name                         | string  | new guild name                                                |    yes   |
| verificationLevel?           | number  | will change the guild's verification level                    |    no    |
| explicitContentFilter?       | number  | will change the guild's content filter level                  |    no    |
| afkChannel?                  | integer | will change the guild's afk voice channel                     |    no    |
| systemChannel?               | integer | will change the guild's system channel                        |    no    |
| afkTimeout?                  | number  | will change the guild's afk timeout in the guild's afkChannel |    no    |
| icon?                        | string  | will change the guild's icon                                  |    no    |
| owner?                       | integer |                                                               |    no    |
| splash?                      | string  | will change the server's invite splash banner                 |    no    |
| discoverySplash?             | string  | will change the server's discovery splash banner              |    no    |
| banner?                      | string  | will change the server's banner                               |    no    |
| defaultMessageNotifications? | number  | will change the guild's default message notifications         |    no    |
| systemChannelFlags?          | number  | will change the server's system flags                         |    no    |
| rulesChannel?                | integer | will change the guild's rules channel                         |    no    |
| publicUpdatesChannel?        | integer | will change the guild's announcement channel                  |    no    |
| preferredLocale?             | string  | will change the guild's preferred locale                      |    no    |
| description?                 | string  | reason that will be displayed in the guild's audit logs       |    no    |
| features?                    | string  | reason that will be displayed in the guild's audit logs       |    no    |

**Note: you can use `$default` to keep the current property.**

<details>
  <summary><h3> Types for Parameters </h3></summary>

**[Default Message Notification Level](https://discord.com/developers/docs/resources/guild#guild-object-default-message-notification-level)**

| KEY           | VALUE | DESCRIPTION                                                                        |
| ------------- | ----- | ---------------------------------------------------------------------------------- |
| ALL_MESSAGES  | 0     | members will receive notifications for all messages by default                     |
| ONLY_MENTIONS | 1     | members will receive notifications only for messages that @mention them by default |

**[Explicit Content Filter Level](https://discord.com/developers/docs/resources/guild#guild-object-explicit-content-filter-level)**

| LEVEL                 | INTEGER | DESCRIPTION                                                 |
| --------------------- | ------- | ----------------------------------------------------------- |
| DISABLED              | 0       | media content will not be scanned                           |
| MEMBERS_WITHOUT_ROLES | 1       | media content sent by members without roles will be scanned |
| ALL_MEMBERS           | 2       | media content sent by all members will be scanned           |
 
**[MFA Level](https://discord.com/developers/docs/resources/guild#guild-object-mfa-level)**

| LEVEL    | INTEGER | DESCRIPTION                                             |
| -------- | ------- | ------------------------------------------------------- |
| NONE     | 0       | guild has no MFA/2FA requirement for moderation actions |
| ELEVATED | 1       | guild has a 2FA requirement for moderation actions      |

**[Verification Level](https://discord.com/developers/docs/resources/guild#guild-object-verification-level)**

| LEVEL     | INTEGER | DESCRIPTION                                               |
| --------- | ------- | --------------------------------------------------------- |
| NONE      | 0       | unrestricted                                              |
| LOW       | 1       | must have verified email on account                       |
| MEDIUM    | 2       | must be registered on Discord for longer than 5 minutes   |
| HIGH      | 3       | must be a member of the server for longer than 10 minutes |
| VERY_HIGH | 4       | must have a verified phone number                         |

**[Guild NSFW Level](https://discord.com/developers/docs/resources/guild#guild-object-guild-nsfw-level)**

| LEVEL          | VALUE |
| -------------- | ----- |
| DEFAULT        | 0     |
| EXPLICIT       | 1     |
| SAFE           | 2     |
| AGE_RESTRICTED | 3     |

**[System Channel Flags](https://discord.com/developers/docs/resources/guild#guild-object-system-channel-flags)**

| LEVEL                                                    | INTEGER | DESCRIPTION                                                   |
| -------------------------------------------------------- | ------- | ------------------------------------------------------------- |
| SUPPRESS_JOIN_NOTIFICATIONS                              | 1 << 0  | Suppress member join notifications                            |
| SUPPRESS_PREMIUM_SUBSCRIPTIONS                           | 1 << 1  | Suppress server boost notifications                           |
| SUPPRESS_GUILD_REMINDER_NOTIFICATIONS                    | 1 << 2  | Suppress server setup tips                                    |
| SUPPRESS_JOIN_NOTIFICATION_REPLIES                       | 1 << 3  | Hide member join sticker reply buttons                        |
| SUPPRESS_ROLE_SUBSCRIPTION_PURCHASE_NOTIFICATIONS        | 1 << 4  | Suppress role subscription purchase and renewal notifications |
| SUPPRESS_ROLE_SUBSCRIPTION_PURCHASE_NOTIFICATION_REPLIES | 1 << 5  | Hide role subscription sticker reply buttons                  |

</details>

## Example

This will change the current guild name to `Example`, set it's **Explicit Content Filter Level** to `HIGH` and **Default Message Notification Level** to `ONLY_MENTIONS`: 

```javascript
bot.command({
  name: 'editGuild',
  code: `
  $editGuild[$guildID;Example;$default;$default;3;$default;$default;$default;$default;$default;$default;$default;$default;1]
  `
});
```
---
title: "channels.updateUsername"
description: "Change the username of a supergroup/channel"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/channels_updateUsername.html
---
# Method: channels.updateUsername
[Back to methods index](index.html)



Change the username of a supergroup/channel

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|channel|[Username, chat ID, Update, Message or InputChannel](/API_docs/types/InputChannel.html) | Channel | Optional|
|username|[string](/API_docs/types/string.html) | New username | Yes|


### Return type: [Bool](/API_docs/types/Bool.html)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Bool = $MadelineProto->channels->updateUsername(['channel' => InputChannel, 'username' => 'string', ]);
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|CHANNEL_INVALID|The provided channel is invalid|
|400|CHANNEL_PRIVATE|You haven't joined this channel/supergroup|
|400|CHANNELS_ADMIN_PUBLIC_TOO_MUCH|You're admin of too many public channels, make some channels private to change the username of this channel|
|400|CHAT_ADMIN_REQUIRED|You must be an admin in this chat to do this|
|400|CHAT_NOT_MODIFIED|The pinned message wasn't modified|
|400|USERNAME_INVALID|The provided username is not valid|
|400|USERNAME_NOT_MODIFIED|The username was not modified|
|400|USERNAME_OCCUPIED|The provided username is already occupied|
|406|AUTH_KEY_DUPLICATED|An auth key with the same ID was already generated|
|403|CHAT_WRITE_FORBIDDEN|You can't write in this chat|



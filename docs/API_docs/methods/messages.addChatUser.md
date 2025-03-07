---
title: "messages.addChatUser"
description: "Adds a user to a chat and sends a service message on it."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_addChatUser.html
---
# Method: messages.addChatUser
[Back to methods index](index.html)



Adds a user to a chat and sends a service message on it.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|chat\_id|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) |  | Optional|
|user\_id|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | User ID to be added | Optional|
|fwd\_limit|[int](/API_docs/types/int.html) | Number of last messages to be forwarded | Yes|


### Return type: [Updates](/API_docs/types/Updates.html)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Updates = $MadelineProto->messages->addChatUser(['chat_id' => InputPeer, 'user_id' => InputUser, 'fwd_limit' => int, ]);
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|CHAT_ADMIN_REQUIRED|You must be an admin in this chat to do this|
|400|CHAT_ID_INVALID|The provided chat id is invalid|
|400|INPUT_USER_DEACTIVATED|The specified user was deleted|
|400|PEER_ID_INVALID|The provided peer id is invalid|
|400|USER_ALREADY_PARTICIPANT|The user is already in the group|
|400|USER_ID_INVALID|The provided user ID is invalid|
|400|USER_IS_BLOCKED|You were blocked by this user|
|400|USER_NOT_MUTUAL_CONTACT|The provided user is not a mutual contact|
|400|USERS_TOO_MUCH|The maximum number of users has been exceeded (to create a chat, for example)|
|400|YOU_BLOCKED_USER|You blocked this user|
|403|CHAT_WRITE_FORBIDDEN|You can't write in this chat|
|403|USER_NOT_MUTUAL_CONTACT|The provided user is not a mutual contact|
|403|USER_PRIVACY_RESTRICTED|The user's privacy settings do not allow you to do this|



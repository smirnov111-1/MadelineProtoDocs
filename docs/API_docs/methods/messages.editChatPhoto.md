---
title: "messages.editChatPhoto"
description: "Changes chat photo and sends a service message on it"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_editChatPhoto.html
---
# Method: messages.editChatPhoto
[Back to methods index](index.html)



Changes chat photo and sends a service message on it

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|chat\_id|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) |  | Optional|
|photo|[InputChatPhoto](/API_docs/types/InputChatPhoto.html) | Photo to be set | Optional|


### Return type: [Updates](/API_docs/types/Updates.html)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Updates = $MadelineProto->messages->editChatPhoto(['chat_id' => InputPeer, 'photo' => InputChatPhoto, ]);
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|CHAT_ID_INVALID|The provided chat id is invalid|
|400|CHAT_NOT_MODIFIED|The pinned message wasn't modified|
|400|INPUT_FETCH_FAIL|Failed deserializing TL payload|
|400|PEER_ID_INVALID|The provided peer id is invalid|
|400|PHOTO_CROP_SIZE_SMALL|Photo is too small|
|400|PHOTO_EXT_INVALID|The extension of the photo is invalid|
|400|PHOTO_INVALID|Photo invalid|



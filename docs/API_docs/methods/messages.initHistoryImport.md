---
title: "messages.initHistoryImport"
description: "messages.initHistoryImport parameters, return type and example"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_initHistoryImport.html
---
# Method: messages.initHistoryImport
[Back to methods index](index.html)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Optional|
|file|[File path or InputFile](/API_docs/types/InputFile.html) | Yes|
|media\_count|[int](/API_docs/types/int.html) | Yes|


### Return type: [messages.HistoryImport](/API_docs/types/messages.HistoryImport.html)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_HistoryImport = $MadelineProto->messages->initHistoryImport(['peer' => InputPeer, 'file' => InputFile, 'media_count' => int, ]);
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|IMPORT_FILE_INVALID|The specified chat export file is invalid|
|400|IMPORT_FORMAT_UNRECOGNIZED|The specified chat export file was exported from an unsupported chat app|
|406|PREVIOUS_CHAT_IMPORT_ACTIVE_WAIT_5MIN|Import for this chat is already in progress, wait 5 minutes before starting a new one.|



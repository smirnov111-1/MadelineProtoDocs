---
title: "phone.exportGroupCallInvite"
description: "phone.exportGroupCallInvite parameters, return type and example"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/phone_exportGroupCallInvite.html
---
# Method: phone.exportGroupCallInvite
[Back to methods index](index.html)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|can\_self\_unmute|[Bool](/API_docs/types/Bool.html) | Optional|
|call|[InputGroupCall](/API_docs/types/InputGroupCall.html) | Yes|


### Return type: [phone.ExportedGroupCallInvite](/API_docs/types/phone.ExportedGroupCallInvite.html)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$phone_ExportedGroupCallInvite = $MadelineProto->phone->exportGroupCallInvite(['can_self_unmute' => Bool, 'call' => InputGroupCall, ]);
```


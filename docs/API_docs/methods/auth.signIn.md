---
title: "auth.signIn"
description: "You cannot use this method directly, use the completePhoneLogin method instead (see https://docs.madelineproto.xyz for more info)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/auth_signIn.html
---
# Method: auth.signIn
[Back to methods index](index.html)



You cannot use this method directly, use the completePhoneLogin method instead (see https://docs.madelineproto.xyz for more info)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|phone\_number|[string](/API_docs/types/string.html) | Phone number in the international format | Yes|
|phone\_code\_hash|[string](/API_docs/types/string.html) | SMS-message ID, obtained from [auth.sendCode](../methods/auth.sendCode.html) | Yes|
|phone\_code|[string](/API_docs/types/string.html) | Valid numerical code from the SMS-message | Yes|


### Return type: [auth.Authorization](/API_docs/types/auth.Authorization.html)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$auth_Authorization = $MadelineProto->auth->signIn(['phone_number' => 'string', 'phone_code_hash' => 'string', 'phone_code' => 'string', ]);
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|PHONE_CODE_EMPTY|phone_code is missing|
|400|PHONE_CODE_EXPIRED|The phone code you provided has expired, this may happen if it was sent to any chat on telegram (if the code is sent through a telegram chat (not the official account) to avoid it append or prepend to the code some chars)|
|400|PHONE_CODE_INVALID|The provided phone code is invalid|
|400|PHONE_NUMBER_INVALID|The phone number is invalid|
|400|PHONE_NUMBER_UNOCCUPIED|The phone number is not yet being used|
|406|PHONE_NUMBER_INVALID|The phone number is invalid|
|406|UPDATE_APP_TO_LOGIN|Please update to the latest version of MadelineProto to login.|
|401|SESSION_PASSWORD_NEEDED|2FA is enabled, use a password to login|



---
title: "messages.getFeaturedStickers"
description: "Get featured stickers"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getFeaturedStickers.html
---
# Method: messages.getFeaturedStickers
[Back to methods index](index.html)



Get featured stickers

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|hash|[long](/API_docs/types/long.html) |  | Yes|


### Return type: [messages.FeaturedStickers](/API_docs/types/messages.FeaturedStickers.html)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_FeaturedStickers = $MadelineProto->messages->getFeaturedStickers(['hash' => long, ]);
```


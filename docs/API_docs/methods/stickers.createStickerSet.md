---
title: "stickers.createStickerSet"
description: "Create a stickerset, bots only."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/stickers_createStickerSet.html
---
# Method: stickers.createStickerSet
[Back to methods index](index.html)



Create a stickerset, bots only.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|masks|[Bool](/API_docs/types/Bool.html) | Whether this is a mask stickerset | Optional|
|animated|[Bool](/API_docs/types/Bool.html) | Whether this is an animated stickerset | Optional|
|user\_id|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | Stickerset owner | Optional|
|title|[string](/API_docs/types/string.html) | Stickerset name, `1-64` chars | Yes|
|short\_name|[string](/API_docs/types/string.html) | Sticker set name. Can contain only English letters, digits and underscores. Must end with *"*by*<bot username="">"</bot>* (*<bot_username></bot_username>* is case insensitive); 1-64 characters | Yes|
|thumb|[MessageMedia, Update, Message or InputDocument](/API_docs/types/InputDocument.html) | Thumbnail | Optional|
|stickers|Array of [InputStickerSetItem](/API_docs/types/InputStickerSetItem.html) | Stickers | Yes|
|software|[string](/API_docs/types/string.html) |  | Optional|


### Return type: [messages.StickerSet](/API_docs/types/messages.StickerSet.html)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_StickerSet = $MadelineProto->stickers->createStickerSet(['masks' => Bool, 'animated' => Bool, 'user_id' => InputUser, 'title' => 'string', 'short_name' => 'string', 'thumb' => InputDocument, 'stickers' => [InputStickerSetItem, InputStickerSetItem], 'software' => 'string', ]);
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|BOT_MISSING|This method can only be run by a bot|
|400|PACK_SHORT_NAME_INVALID|Short pack name invalid|
|400|PACK_SHORT_NAME_OCCUPIED|A stickerpack with this name already exists|
|400|PACK_TITLE_INVALID|The stickerpack title is invalid|
|400|PEER_ID_INVALID|The provided peer id is invalid|
|400|SHORTNAME_OCCUPY_FAILED|An internal error occurred|
|400|STICKER_EMOJI_INVALID|Sticker emoji invalid|
|400|STICKER_FILE_INVALID|Sticker file invalid|
|400|STICKER_PNG_DIMENSIONS|Sticker png dimensions invalid|
|400|STICKER_PNG_NOPNG|One of the specified stickers is not a valid PNG file|
|400|STICKER_TGS_NODOC|Incorrect document type for sticker.|
|400|STICKER_TGS_NOTGS|Invalid TGS sticker provided.|
|400|STICKER_THUMB_PNG_NOPNG|Incorrect stickerset thumb file provided, PNG / WEBP expected.|
|400|STICKER_THUMB_TGS_NOTGS|Incorrect stickerset TGS thumb file provided.|
|400|STICKERS_EMPTY|No sticker provided|
|400|USER_ID_INVALID|The provided user ID is invalid|



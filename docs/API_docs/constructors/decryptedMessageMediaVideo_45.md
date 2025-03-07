---
title: "decryptedMessageMediaVideo"
description: "Video attached to an encrypted message."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: decryptedMessageMediaVideo\_45  
[Back to constructors index](/API_docs/constructors/index.html)



Video attached to an encrypted message.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|thumb|[bytes](/API_docs/types/bytes.html) | Yes|Content of thumbnail file (JPEG file, quality 55, set in a square 90x90)|
|thumb\_w|[int](/API_docs/types/int.html) | Yes|Thumbnail width|
|thumb\_h|[int](/API_docs/types/int.html) | Yes|Thumbnail height|
|duration|[int](/API_docs/types/int.html) | Yes|Duration of video in seconds|
|mime\_type|[string](/API_docs/types/string.html) | Yes|MIME-type of the video file<br>Parameter added in [Layer 17](https://core.telegram.org/api/layers#layer-17).|
|w|[int](/API_docs/types/int.html) | Yes|Image width|
|h|[int](/API_docs/types/int.html) | Yes|Image height|
|size|[int](/API_docs/types/int.html) | Yes|File size|
|caption|[string](/API_docs/types/string.html) | Yes|Caption|



### Type: [DecryptedMessageMedia](/API_docs/types/DecryptedMessageMedia.html)


### Example:

```php
$decryptedMessageMediaVideo_45 = ['_' => 'decryptedMessageMediaVideo', 'thumb' => 'bytes', 'thumb_w' => int, 'thumb_h' => int, 'duration' => int, 'mime_type' => 'string', 'w' => int, 'h' => int, 'size' => int, 'caption' => 'string'];
```  

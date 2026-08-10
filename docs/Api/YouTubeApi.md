# ScrapeBadger\YouTubeApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**youtubeBatchVideoDetail()**](YouTubeApi.md#youtubeBatchVideoDetail) | **POST** /v1/youtube/videos/batch | Batch video detail |
| [**youtubeChannelAbout()**](YouTubeApi.md#youtubeChannelAbout) | **GET** /v1/youtube/channels/{channel_id}/about | Channel about |
| [**youtubeChannelPlaylists()**](YouTubeApi.md#youtubeChannelPlaylists) | **GET** /v1/youtube/channels/{channel_id}/playlists | Channel playlists |
| [**youtubeChannelShorts()**](YouTubeApi.md#youtubeChannelShorts) | **GET** /v1/youtube/channels/{channel_id}/shorts | Channel shorts |
| [**youtubeChannelStreams()**](YouTubeApi.md#youtubeChannelStreams) | **GET** /v1/youtube/channels/{channel_id}/streams | Channel streams |
| [**youtubeChannelVideos()**](YouTubeApi.md#youtubeChannelVideos) | **GET** /v1/youtube/channels/{channel_id}/videos | Channel videos |
| [**youtubeCommentReplies()**](YouTubeApi.md#youtubeCommentReplies) | **GET** /v1/youtube/videos/{video_id}/comments/{comment_id}/replies | Comment replies |
| [**youtubeCommunityPostComments()**](YouTubeApi.md#youtubeCommunityPostComments) | **GET** /v1/youtube/posts/{post_id}/comments | Community post comments |
| [**youtubeCommunityPosts()**](YouTubeApi.md#youtubeCommunityPosts) | **GET** /v1/youtube/channels/{channel_id}/community | Community posts |
| [**youtubeContentRegions()**](YouTubeApi.md#youtubeContentRegions) | **GET** /v1/youtube/regions | Content regions |
| [**youtubeGetACommunityPost()**](YouTubeApi.md#youtubeGetACommunityPost) | **GET** /v1/youtube/posts/{post_id} | Get a community post |
| [**youtubeGetAMixRadioQueue()**](YouTubeApi.md#youtubeGetAMixRadioQueue) | **GET** /v1/youtube/mixes/{playlist_id} | Get a mix / radio queue |
| [**youtubeGetAShort()**](YouTubeApi.md#youtubeGetAShort) | **GET** /v1/youtube/shorts/{video_id} | Get a Short |
| [**youtubeGetChannelDetail()**](YouTubeApi.md#youtubeGetChannelDetail) | **GET** /v1/youtube/channels/{channel_id} | Get channel detail |
| [**youtubeGetPlaylistDetail()**](YouTubeApi.md#youtubeGetPlaylistDetail) | **GET** /v1/youtube/playlists/{playlist_id} | Get playlist detail |
| [**youtubeGetVideoDetail()**](YouTubeApi.md#youtubeGetVideoDetail) | **GET** /v1/youtube/videos/{video_id} | Get video detail |
| [**youtubeGuestHomeFeed()**](YouTubeApi.md#youtubeGuestHomeFeed) | **GET** /v1/youtube/home | Guest home feed |
| [**youtubeKeywordSuggestions()**](YouTubeApi.md#youtubeKeywordSuggestions) | **GET** /v1/youtube/autocomplete | Keyword suggestions |
| [**youtubeListCaptionTracks()**](YouTubeApi.md#youtubeListCaptionTracks) | **GET** /v1/youtube/videos/{video_id}/captions | List caption tracks |
| [**youtubeLiveChatMessages()**](YouTubeApi.md#youtubeLiveChatMessages) | **GET** /v1/youtube/videos/{video_id}/live_chat | Live chat messages |
| [**youtubeOembedMetadata()**](YouTubeApi.md#youtubeOembedMetadata) | **GET** /v1/youtube/oembed | oEmbed metadata |
| [**youtubePlaylistItemsPage()**](YouTubeApi.md#youtubePlaylistItemsPage) | **GET** /v1/youtube/playlists/{playlist_id}/items | Playlist items page |
| [**youtubeRelatedVideos()**](YouTubeApi.md#youtubeRelatedVideos) | **GET** /v1/youtube/videos/{video_id}/related | Related videos |
| [**youtubeResolveHandleUrlToId()**](YouTubeApi.md#youtubeResolveHandleUrlToId) | **GET** /v1/youtube/channels/resolve | Resolve handle/URL to id |
| [**youtubeSearchWithinAChannel()**](YouTubeApi.md#youtubeSearchWithinAChannel) | **GET** /v1/youtube/channels/{channel_id}/search | Search within a channel |
| [**youtubeSearchYoutube()**](YouTubeApi.md#youtubeSearchYoutube) | **GET** /v1/youtube/search | Search YouTube |
| [**youtubeSearchYoutubeMusic()**](YouTubeApi.md#youtubeSearchYoutubeMusic) | **GET** /v1/youtube/music/search | Search YouTube Music |
| [**youtubeShortsBySound()**](YouTubeApi.md#youtubeShortsBySound) | **GET** /v1/youtube/shorts/by_sound/{sound_id} | Shorts by sound |
| [**youtubeStreamFormats()**](YouTubeApi.md#youtubeStreamFormats) | **GET** /v1/youtube/videos/{video_id}/streams | Stream formats |
| [**youtubeSubscriberCountFast()**](YouTubeApi.md#youtubeSubscriberCountFast) | **GET** /v1/youtube/channels/{channel_id}/subscriber_count | Subscriber count (fast) |
| [**youtubeSupportedMarkets()**](YouTubeApi.md#youtubeSupportedMarkets) | **GET** /v1/youtube/markets | Supported markets |
| [**youtubeTrendingShorts()**](YouTubeApi.md#youtubeTrendingShorts) | **GET** /v1/youtube/trending/shorts | Trending shorts |
| [**youtubeTrendingVideos()**](YouTubeApi.md#youtubeTrendingVideos) | **GET** /v1/youtube/trending | Trending videos |
| [**youtubeUiLanguages()**](YouTubeApi.md#youtubeUiLanguages) | **GET** /v1/youtube/languages | UI languages |
| [**youtubeVideoCategories()**](YouTubeApi.md#youtubeVideoCategories) | **GET** /v1/youtube/categories | Video categories |
| [**youtubeVideoComments()**](YouTubeApi.md#youtubeVideoComments) | **GET** /v1/youtube/videos/{video_id}/comments | Video comments |
| [**youtubeVideoTranscript()**](YouTubeApi.md#youtubeVideoTranscript) | **GET** /v1/youtube/videos/{video_id}/transcript | Video transcript |
| [**youtubeVideosUnderAHashtag()**](YouTubeApi.md#youtubeVideosUnderAHashtag) | **GET** /v1/youtube/hashtags/{tag} | Videos under a hashtag |
| [**youtubeYoutubeScraperHealthCheck()**](YouTubeApi.md#youtubeYoutubeScraperHealthCheck) | **GET** /v1/youtube/health | YouTube scraper health check |
| [**youtubeYoutubeScraperHealthCheckHead()**](YouTubeApi.md#youtubeYoutubeScraperHealthCheckHead) | **HEAD** /v1/youtube/health | YouTube scraper health check |


## `youtubeBatchVideoDetail()`

```php
youtubeBatchVideoDetail($request_body): mixed
```

Batch video detail

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request_body = NULL; // array<string,mixed>

try {
    $result = $apiInstance->youtubeBatchVideoDetail($request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeBatchVideoDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request_body** | [**array<string,mixed>**](../Model/mixed.md)|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeChannelAbout()`

```php
youtubeChannelAbout($channel_id): mixed
```

Channel about

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string

try {
    $result = $apiInstance->youtubeChannelAbout($channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeChannelAbout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeChannelPlaylists()`

```php
youtubeChannelPlaylists($channel_id): mixed
```

Channel playlists

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string

try {
    $result = $apiInstance->youtubeChannelPlaylists($channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeChannelPlaylists: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeChannelShorts()`

```php
youtubeChannelShorts($channel_id): mixed
```

Channel shorts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string

try {
    $result = $apiInstance->youtubeChannelShorts($channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeChannelShorts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeChannelStreams()`

```php
youtubeChannelStreams($channel_id): mixed
```

Channel streams

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string

try {
    $result = $apiInstance->youtubeChannelStreams($channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeChannelStreams: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeChannelVideos()`

```php
youtubeChannelVideos($channel_id): mixed
```

Channel videos

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string

try {
    $result = $apiInstance->youtubeChannelVideos($channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeChannelVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeCommentReplies()`

```php
youtubeCommentReplies($video_id, $comment_id, $continuation): mixed
```

Comment replies

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string
$comment_id = 'comment_id_example'; // string
$continuation = 'continuation_example'; // string | Replies continuation token

try {
    $result = $apiInstance->youtubeCommentReplies($video_id, $comment_id, $continuation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeCommentReplies: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |
| **comment_id** | **string**|  | |
| **continuation** | **string**| Replies continuation token | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeCommunityPostComments()`

```php
youtubeCommunityPostComments($post_id): mixed
```

Community post comments

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_id = 'post_id_example'; // string

try {
    $result = $apiInstance->youtubeCommunityPostComments($post_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeCommunityPostComments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeCommunityPosts()`

```php
youtubeCommunityPosts($channel_id): mixed
```

Community posts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string

try {
    $result = $apiInstance->youtubeCommunityPosts($channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeCommunityPosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeContentRegions()`

```php
youtubeContentRegions(): mixed
```

Content regions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->youtubeContentRegions();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeContentRegions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeGetACommunityPost()`

```php
youtubeGetACommunityPost($post_id): mixed
```

Get a community post

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_id = 'post_id_example'; // string

try {
    $result = $apiInstance->youtubeGetACommunityPost($post_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeGetACommunityPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeGetAMixRadioQueue()`

```php
youtubeGetAMixRadioQueue($playlist_id): mixed
```

Get a mix / radio queue

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$playlist_id = 'playlist_id_example'; // string

try {
    $result = $apiInstance->youtubeGetAMixRadioQueue($playlist_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeGetAMixRadioQueue: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **playlist_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeGetAShort()`

```php
youtubeGetAShort($video_id): mixed
```

Get a Short

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string

try {
    $result = $apiInstance->youtubeGetAShort($video_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeGetAShort: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeGetChannelDetail()`

```php
youtubeGetChannelDetail($channel_id, $gl, $hl): mixed
```

Get channel detail

Channel detail (accepts a UC id, @handle, or custom URL).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string
$gl = 'gl_example'; // string
$hl = 'hl_example'; // string

try {
    $result = $apiInstance->youtubeGetChannelDetail($channel_id, $gl, $hl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeGetChannelDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |
| **gl** | **string**|  | [optional] |
| **hl** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeGetPlaylistDetail()`

```php
youtubeGetPlaylistDetail($playlist_id): mixed
```

Get playlist detail

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$playlist_id = 'playlist_id_example'; // string

try {
    $result = $apiInstance->youtubeGetPlaylistDetail($playlist_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeGetPlaylistDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **playlist_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeGetVideoDetail()`

```php
youtubeGetVideoDetail($video_id, $gl, $hl): mixed
```

Get video detail

Full video detail — merged player + next (likes, comments, chapters, related).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string
$gl = 'gl_example'; // string
$hl = 'hl_example'; // string

try {
    $result = $apiInstance->youtubeGetVideoDetail($video_id, $gl, $hl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeGetVideoDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |
| **gl** | **string**|  | [optional] |
| **hl** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeGuestHomeFeed()`

```php
youtubeGuestHomeFeed(): mixed
```

Guest home feed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->youtubeGuestHomeFeed();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeGuestHomeFeed: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeKeywordSuggestions()`

```php
youtubeKeywordSuggestions($query, $gl, $hl): mixed
```

Keyword suggestions

Return YouTube keyword autocomplete suggestions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial query prefix
$gl = 'gl_example'; // string
$hl = 'hl_example'; // string

try {
    $result = $apiInstance->youtubeKeywordSuggestions($query, $gl, $hl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeKeywordSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial query prefix | |
| **gl** | **string**|  | [optional] |
| **hl** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeListCaptionTracks()`

```php
youtubeListCaptionTracks($video_id): mixed
```

List caption tracks

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string

try {
    $result = $apiInstance->youtubeListCaptionTracks($video_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeListCaptionTracks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeLiveChatMessages()`

```php
youtubeLiveChatMessages($video_id, $continuation, $replay): mixed
```

Live chat messages

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string
$continuation = 'continuation_example'; // string
$replay = false; // bool

try {
    $result = $apiInstance->youtubeLiveChatMessages($video_id, $continuation, $replay);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeLiveChatMessages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |
| **continuation** | **string**|  | [optional] |
| **replay** | **bool**|  | [optional] [default to false] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeOembedMetadata()`

```php
youtubeOembedMetadata($url): mixed
```

oEmbed metadata

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$url = 'url_example'; // string | A YouTube URL

try {
    $result = $apiInstance->youtubeOembedMetadata($url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeOembedMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **url** | **string**| A YouTube URL | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubePlaylistItemsPage()`

```php
youtubePlaylistItemsPage($playlist_id): mixed
```

Playlist items page

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$playlist_id = 'playlist_id_example'; // string

try {
    $result = $apiInstance->youtubePlaylistItemsPage($playlist_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubePlaylistItemsPage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **playlist_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeRelatedVideos()`

```php
youtubeRelatedVideos($video_id): mixed
```

Related videos

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string

try {
    $result = $apiInstance->youtubeRelatedVideos($video_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeRelatedVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeResolveHandleUrlToId()`

```php
youtubeResolveHandleUrlToId($handle, $url): mixed
```

Resolve handle/URL to id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$handle = 'handle_example'; // string
$url = 'url_example'; // string

try {
    $result = $apiInstance->youtubeResolveHandleUrlToId($handle, $url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeResolveHandleUrlToId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **handle** | **string**|  | [optional] |
| **url** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeSearchWithinAChannel()`

```php
youtubeSearchWithinAChannel($channel_id, $query): mixed
```

Search within a channel

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string
$query = 'query_example'; // string | Search keywords

try {
    $result = $apiInstance->youtubeSearchWithinAChannel($channel_id, $query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeSearchWithinAChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |
| **query** | **string**| Search keywords | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeSearchYoutube()`

```php
youtubeSearchYoutube($query, $type, $sort_by, $upload_date, $duration, $features, $gl, $hl, $continuation): mixed
```

Search YouTube

Search videos / channels / playlists with the full filter matrix.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords
$type = 'type_example'; // string | video|channel|playlist|movie|all
$sort_by = 'sort_by_example'; // string | relevance|date|views|rating
$upload_date = 'upload_date_example'; // string | hour|today|week|month|year
$duration = 'duration_example'; // string | short|medium|long
$features = 'features_example'; // string | hd,4k,360,vr180,3d,hdr,cc,subtitles,live
$gl = 'gl_example'; // string | Content region (US, GB, DE…)
$hl = 'hl_example'; // string | UI language
$continuation = 'continuation_example'; // string

try {
    $result = $apiInstance->youtubeSearchYoutube($query, $type, $sort_by, $upload_date, $duration, $features, $gl, $hl, $continuation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeSearchYoutube: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords | |
| **type** | **string**| video|channel|playlist|movie|all | [optional] |
| **sort_by** | **string**| relevance|date|views|rating | [optional] |
| **upload_date** | **string**| hour|today|week|month|year | [optional] |
| **duration** | **string**| short|medium|long | [optional] |
| **features** | **string**| hd,4k,360,vr180,3d,hdr,cc,subtitles,live | [optional] |
| **gl** | **string**| Content region (US, GB, DE…) | [optional] |
| **hl** | **string**| UI language | [optional] |
| **continuation** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeSearchYoutubeMusic()`

```php
youtubeSearchYoutubeMusic($query): mixed
```

Search YouTube Music

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords

try {
    $result = $apiInstance->youtubeSearchYoutubeMusic($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeSearchYoutubeMusic: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeShortsBySound()`

```php
youtubeShortsBySound($sound_id): mixed
```

Shorts by sound

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sound_id = 'sound_id_example'; // string

try {
    $result = $apiInstance->youtubeShortsBySound($sound_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeShortsBySound: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sound_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeStreamFormats()`

```php
youtubeStreamFormats($video_id, $client): mixed
```

Stream formats

Stream/format metadata (best-effort; media URLs may be PO-token gated).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string
$client = 'IOS'; // string | IOS|ANDROID|WEB

try {
    $result = $apiInstance->youtubeStreamFormats($video_id, $client);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeStreamFormats: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |
| **client** | **string**| IOS|ANDROID|WEB | [optional] [default to &#39;IOS&#39;] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeSubscriberCountFast()`

```php
youtubeSubscriberCountFast($channel_id): mixed
```

Subscriber count (fast)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string

try {
    $result = $apiInstance->youtubeSubscriberCountFast($channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeSubscriberCountFast: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeSupportedMarkets()`

```php
youtubeSupportedMarkets(): mixed
```

Supported markets

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->youtubeSupportedMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeSupportedMarkets: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeTrendingShorts()`

```php
youtubeTrendingShorts(): mixed
```

Trending shorts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->youtubeTrendingShorts();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeTrendingShorts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeTrendingVideos()`

```php
youtubeTrendingVideos($gl, $type): mixed
```

Trending videos

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$gl = 'gl_example'; // string
$type = 'now'; // string | now|music|gaming|movies

try {
    $result = $apiInstance->youtubeTrendingVideos($gl, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeTrendingVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **gl** | **string**|  | [optional] |
| **type** | **string**| now|music|gaming|movies | [optional] [default to &#39;now&#39;] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeUiLanguages()`

```php
youtubeUiLanguages(): mixed
```

UI languages

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->youtubeUiLanguages();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeUiLanguages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeVideoCategories()`

```php
youtubeVideoCategories($gl): mixed
```

Video categories

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$gl = 'US'; // string

try {
    $result = $apiInstance->youtubeVideoCategories($gl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeVideoCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **gl** | **string**|  | [optional] [default to &#39;US&#39;] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeVideoComments()`

```php
youtubeVideoComments($video_id, $sort_by, $continuation): mixed
```

Video comments

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string
$sort_by = 'top'; // string | top|newest
$continuation = 'continuation_example'; // string

try {
    $result = $apiInstance->youtubeVideoComments($video_id, $sort_by, $continuation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeVideoComments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |
| **sort_by** | **string**| top|newest | [optional] [default to &#39;top&#39;] |
| **continuation** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeVideoTranscript()`

```php
youtubeVideoTranscript($video_id, $language): mixed
```

Video transcript

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string
$language = 'language_example'; // string | BCP-47 language code

try {
    $result = $apiInstance->youtubeVideoTranscript($video_id, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeVideoTranscript: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |
| **language** | **string**| BCP-47 language code | [optional] |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeVideosUnderAHashtag()`

```php
youtubeVideosUnderAHashtag($tag): mixed
```

Videos under a hashtag

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tag = 'tag_example'; // string

try {
    $result = $apiInstance->youtubeVideosUnderAHashtag($tag);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeVideosUnderAHashtag: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tag** | **string**|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeYoutubeScraperHealthCheck()`

```php
youtubeYoutubeScraperHealthCheck(): mixed
```

YouTube scraper health check

Check health of the YouTube scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->youtubeYoutubeScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeYoutubeScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `youtubeYoutubeScraperHealthCheckHead()`

```php
youtubeYoutubeScraperHealthCheckHead(): mixed
```

YouTube scraper health check

Check health of the YouTube scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YouTubeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->youtubeYoutubeScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YouTubeApi->youtubeYoutubeScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

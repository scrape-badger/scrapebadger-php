# ScrapeBadger\TikTokApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**tiktokGeneralSearch()**](TikTokApi.md#tiktokGeneralSearch) | **GET** /v1/tiktok/search | General search |
| [**tiktokGetCommentReplies()**](TikTokApi.md#tiktokGetCommentReplies) | **GET** /v1/tiktok/comments/{comment_id}/replies | Get comment replies |
| [**tiktokGetComments()**](TikTokApi.md#tiktokGetComments) | **GET** /v1/tiktok/videos/{video_id}/comments | Get comments |
| [**tiktokGetFollowersDeprecated()**](TikTokApi.md#tiktokGetFollowersDeprecated) | **GET** /v1/tiktok/users/{username}/followers | Get followers (deprecated) |
| [**tiktokGetFollowingDeprecated()**](TikTokApi.md#tiktokGetFollowingDeprecated) | **GET** /v1/tiktok/users/{username}/following | Get following (deprecated) |
| [**tiktokGetHashtagDetail()**](TikTokApi.md#tiktokGetHashtagDetail) | **GET** /v1/tiktok/hashtags/{name} | Get hashtag detail |
| [**tiktokGetHashtagVideos()**](TikTokApi.md#tiktokGetHashtagVideos) | **GET** /v1/tiktok/hashtags/{name}/videos | Get hashtag videos |
| [**tiktokGetLikedVideosDeprecated()**](TikTokApi.md#tiktokGetLikedVideosDeprecated) | **GET** /v1/tiktok/users/{username}/liked | Get liked videos (deprecated) |
| [**tiktokGetMusicSoundDetail()**](TikTokApi.md#tiktokGetMusicSoundDetail) | **GET** /v1/tiktok/music/{music_id} | Get music/sound detail |
| [**tiktokGetMusicVideos()**](TikTokApi.md#tiktokGetMusicVideos) | **GET** /v1/tiktok/music/{music_id}/videos | Get music videos |
| [**tiktokGetOembedMetadata()**](TikTokApi.md#tiktokGetOembedMetadata) | **GET** /v1/tiktok/oembed | Get oEmbed metadata |
| [**tiktokGetRelatedVideos()**](TikTokApi.md#tiktokGetRelatedVideos) | **GET** /v1/tiktok/videos/{video_id}/related | Get related videos |
| [**tiktokGetReposts()**](TikTokApi.md#tiktokGetReposts) | **GET** /v1/tiktok/users/{username}/reposts | Get reposts |
| [**tiktokGetTiktokAdDetail()**](TikTokApi.md#tiktokGetTiktokAdDetail) | **GET** /v1/tiktok/ads/{ad_id} | Get TikTok ad detail |
| [**tiktokGetTranscript()**](TikTokApi.md#tiktokGetTranscript) | **GET** /v1/tiktok/videos/{video_id}/transcript | Get transcript |
| [**tiktokGetUserProfile()**](TikTokApi.md#tiktokGetUserProfile) | **GET** /v1/tiktok/users/{username} | Get user profile |
| [**tiktokGetUserVideos()**](TikTokApi.md#tiktokGetUserVideos) | **GET** /v1/tiktok/users/{username}/videos | Get user videos |
| [**tiktokGetVideoDetail()**](TikTokApi.md#tiktokGetVideoDetail) | **GET** /v1/tiktok/videos/{video_id} | Get video detail |
| [**tiktokHealthCheck()**](TikTokApi.md#tiktokHealthCheck) | **GET** /v1/tiktok/health | Health check |
| [**tiktokHealthCheckHead()**](TikTokApi.md#tiktokHealthCheckHead) | **HEAD** /v1/tiktok/health | Health check |
| [**tiktokListRegions()**](TikTokApi.md#tiktokListRegions) | **GET** /v1/tiktok/regions | List regions |
| [**tiktokSearchHashtags()**](TikTokApi.md#tiktokSearchHashtags) | **GET** /v1/tiktok/search/hashtags | Search hashtags |
| [**tiktokSearchTheTiktokAdLibrary()**](TikTokApi.md#tiktokSearchTheTiktokAdLibrary) | **GET** /v1/tiktok/ads/search | Search the TikTok Ad Library |
| [**tiktokSearchTiktokAdvertisers()**](TikTokApi.md#tiktokSearchTiktokAdvertisers) | **GET** /v1/tiktok/ads/advertisers | Search TikTok advertisers |
| [**tiktokSearchUsers()**](TikTokApi.md#tiktokSearchUsers) | **GET** /v1/tiktok/search/users | Search users |
| [**tiktokSearchVideos()**](TikTokApi.md#tiktokSearchVideos) | **GET** /v1/tiktok/search/videos | Search videos |
| [**tiktokTrendingHashtags()**](TikTokApi.md#tiktokTrendingHashtags) | **GET** /v1/tiktok/trending/hashtags | Trending hashtags |
| [**tiktokTrendingSongs()**](TikTokApi.md#tiktokTrendingSongs) | **GET** /v1/tiktok/trending/songs | Trending songs |
| [**tiktokTrendingVideos()**](TikTokApi.md#tiktokTrendingVideos) | **GET** /v1/tiktok/trending/videos | Trending videos |


## `tiktokGeneralSearch()`

```php
tiktokGeneralSearch($query, $region, $count, $cursor): mixed
```

General search

General TikTok search — video results from the Top feed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keyword
$region = 'US'; // string
$count = 20; // int
$cursor = 'cursor_example'; // string | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor

try {
    $result = $apiInstance->tiktokGeneralSearch($query, $region, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGeneralSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keyword | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 20] |
| **cursor** | **string**| Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

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

## `tiktokGetCommentReplies()`

```php
tiktokGetCommentReplies($comment_id, $video_id, $region, $count, $cursor): mixed
```

Get comment replies

Get replies to a TikTok comment (best-effort).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$comment_id = 'comment_id_example'; // string
$video_id = 'video_id_example'; // string | Parent video id
$region = 'US'; // string
$count = 20; // int
$cursor = 'cursor_example'; // string | Pagination cursor from a prior page's pagination.cursor

try {
    $result = $apiInstance->tiktokGetCommentReplies($comment_id, $video_id, $region, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetCommentReplies: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **comment_id** | **string**|  | |
| **video_id** | **string**| Parent video id | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 20] |
| **cursor** | **string**| Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

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

## `tiktokGetComments()`

```php
tiktokGetComments($video_id, $region, $count, $cursor): mixed
```

Get comments

Get top-level comments on a TikTok video.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string
$region = 'US'; // string
$count = 20; // int
$cursor = 'cursor_example'; // string | Pagination cursor from a prior page's pagination.cursor

try {
    $result = $apiInstance->tiktokGetComments($video_id, $region, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetComments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 20] |
| **cursor** | **string**| Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

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

## `tiktokGetFollowersDeprecated()`

```php
tiktokGetFollowersDeprecated($username, $region, $count): mixed
```

Get followers (deprecated)

DEPRECATED — TikTok followers require an authenticated account session. Returns HTTP 410.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$region = 'US'; // string
$count = 30; // int

try {
    $result = $apiInstance->tiktokGetFollowersDeprecated($username, $region, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetFollowersDeprecated: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 30] |

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

## `tiktokGetFollowingDeprecated()`

```php
tiktokGetFollowingDeprecated($username, $region, $count): mixed
```

Get following (deprecated)

DEPRECATED — TikTok following requires an authenticated account session. Returns HTTP 410.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$region = 'US'; // string
$count = 30; // int

try {
    $result = $apiInstance->tiktokGetFollowingDeprecated($username, $region, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetFollowingDeprecated: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 30] |

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

## `tiktokGetHashtagDetail()`

```php
tiktokGetHashtagDetail($name, $region): mixed
```

Get hashtag detail

Get TikTok hashtag/challenge detail.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = 'name_example'; // string
$region = 'US'; // string

try {
    $result = $apiInstance->tiktokGetHashtagDetail($name, $region);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetHashtagDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **name** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |

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

## `tiktokGetHashtagVideos()`

```php
tiktokGetHashtagVideos($name, $region, $count, $cursor): mixed
```

Get hashtag videos

Get videos tagged with a TikTok hashtag.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = 'name_example'; // string
$region = 'US'; // string
$count = 30; // int
$cursor = 'cursor_example'; // string | Pagination cursor from a prior page's pagination.cursor

try {
    $result = $apiInstance->tiktokGetHashtagVideos($name, $region, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetHashtagVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **name** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 30] |
| **cursor** | **string**| Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

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

## `tiktokGetLikedVideosDeprecated()`

```php
tiktokGetLikedVideosDeprecated($username, $region, $count): mixed
```

Get liked videos (deprecated)

DEPRECATED — TikTok liked videos require an authenticated account session. Returns HTTP 410.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$region = 'US'; // string
$count = 30; // int

try {
    $result = $apiInstance->tiktokGetLikedVideosDeprecated($username, $region, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetLikedVideosDeprecated: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 30] |

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

## `tiktokGetMusicSoundDetail()`

```php
tiktokGetMusicSoundDetail($music_id, $region): mixed
```

Get music/sound detail

Get TikTok sound/music detail.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$music_id = 'music_id_example'; // string
$region = 'US'; // string

try {
    $result = $apiInstance->tiktokGetMusicSoundDetail($music_id, $region);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetMusicSoundDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **music_id** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |

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

## `tiktokGetMusicVideos()`

```php
tiktokGetMusicVideos($music_id, $region, $count, $cursor): mixed
```

Get music videos

Get videos using a given TikTok sound.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$music_id = 'music_id_example'; // string
$region = 'US'; // string
$count = 30; // int
$cursor = 'cursor_example'; // string | Pagination cursor from a prior page's pagination.cursor

try {
    $result = $apiInstance->tiktokGetMusicVideos($music_id, $region, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetMusicVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **music_id** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 30] |
| **cursor** | **string**| Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

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

## `tiktokGetOembedMetadata()`

```php
tiktokGetOembedMetadata($url, $region): mixed
```

Get oEmbed metadata

Get cheap unauthenticated oEmbed metadata for a TikTok URL.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$url = 'url_example'; // string | Full TikTok video or profile URL
$region = 'US'; // string

try {
    $result = $apiInstance->tiktokGetOembedMetadata($url, $region);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetOembedMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **url** | **string**| Full TikTok video or profile URL | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |

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

## `tiktokGetRelatedVideos()`

```php
tiktokGetRelatedVideos($video_id, $region, $count): mixed
```

Get related videos

Get TikTok's related videos for a given video.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string
$region = 'US'; // string
$count = 16; // int

try {
    $result = $apiInstance->tiktokGetRelatedVideos($video_id, $region, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetRelatedVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 16] |

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

## `tiktokGetReposts()`

```php
tiktokGetReposts($username, $region, $count): mixed
```

Get reposts

Get videos a TikTok user has reposted.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$region = 'US'; // string
$count = 30; // int

try {
    $result = $apiInstance->tiktokGetReposts($username, $region, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetReposts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 30] |

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

## `tiktokGetTiktokAdDetail()`

```php
tiktokGetTiktokAdDetail($ad_id, $region): mixed
```

Get TikTok ad detail

Get a single ad's advertiser, creatives, and targeting/impression breakdown.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ad_id = 'ad_id_example'; // string
$region = 'DE'; // string | EU region code (the Ad Library is EU-only)

try {
    $result = $apiInstance->tiktokGetTiktokAdDetail($ad_id, $region);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetTiktokAdDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ad_id** | **string**|  | |
| **region** | **string**| EU region code (the Ad Library is EU-only) | [optional] [default to &#39;DE&#39;] |

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

## `tiktokGetTranscript()`

```php
tiktokGetTranscript($video_id, $region): mixed
```

Get transcript

Get subtitle/caption tracks for a TikTok video.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string
$region = 'US'; // string

try {
    $result = $apiInstance->tiktokGetTranscript($video_id, $region);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetTranscript: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |

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

## `tiktokGetUserProfile()`

```php
tiktokGetUserProfile($username, $region): mixed
```

Get user profile

Get a TikTok user's full profile.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$region = 'US'; // string | Content region (ISO 3166-1 alpha-2)

try {
    $result = $apiInstance->tiktokGetUserProfile($username, $region);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetUserProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **region** | **string**| Content region (ISO 3166-1 alpha-2) | [optional] [default to &#39;US&#39;] |

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

## `tiktokGetUserVideos()`

```php
tiktokGetUserVideos($username, $region, $count, $cursor): mixed
```

Get user videos

Get a TikTok user's posted videos.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$region = 'US'; // string
$count = 30; // int
$cursor = 'cursor_example'; // string | Pagination cursor from a prior page's `pagination.cursor` (signer path only).

try {
    $result = $apiInstance->tiktokGetUserVideos($username, $region, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetUserVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 30] |
| **cursor** | **string**| Pagination cursor from a prior page&#39;s &#x60;pagination.cursor&#x60; (signer path only). | [optional] |

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

## `tiktokGetVideoDetail()`

```php
tiktokGetVideoDetail($video_id, $region, $username): mixed
```

Get video detail

Get full metadata for a single TikTok video/post.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$video_id = 'video_id_example'; // string
$region = 'US'; // string
$username = 'username_example'; // string | Author handle (skips oEmbed lookup)

try {
    $result = $apiInstance->tiktokGetVideoDetail($video_id, $region, $username);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokGetVideoDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **video_id** | **string**|  | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **username** | **string**| Author handle (skips oEmbed lookup) | [optional] |

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

## `tiktokHealthCheck()`

```php
tiktokHealthCheck(): mixed
```

Health check

Check health of the TikTok scraper service.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->tiktokHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `tiktokHealthCheckHead()`

```php
tiktokHealthCheckHead(): mixed
```

Health check

Check health of the TikTok scraper service.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->tiktokHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `tiktokListRegions()`

```php
tiktokListRegions(): mixed
```

List regions

List supported TikTok content regions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->tiktokListRegions();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokListRegions: ', $e->getMessage(), PHP_EOL;
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

## `tiktokSearchHashtags()`

```php
tiktokSearchHashtags($query, $region, $count, $cursor): mixed
```

Search hashtags

Search TikTok hashtags by keyword.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keyword
$region = 'US'; // string
$count = 20; // int
$cursor = 'cursor_example'; // string | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor

try {
    $result = $apiInstance->tiktokSearchHashtags($query, $region, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokSearchHashtags: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keyword | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 20] |
| **cursor** | **string**| Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

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

## `tiktokSearchTheTiktokAdLibrary()`

```php
tiktokSearchTheTiktokAdLibrary($query, $advertiser_id, $region, $days, $sort, $offset, $search_id, $count): mixed
```

Search the TikTok Ad Library

Search TikTok's Commercial Content Library (ad transparency) by keyword or advertiser.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = ''; // string | Keyword (ignored when advertiser_id is set)
$advertiser_id = ''; // string | Advertiser business id(s) for advertiser search
$region = 'DE'; // string | EU region code (the Ad Library is EU-only)
$days = 30; // int
$sort = 'last_shown_date,desc'; // string
$offset = 0; // int
$search_id = ''; // string
$count = 20; // int

try {
    $result = $apiInstance->tiktokSearchTheTiktokAdLibrary($query, $advertiser_id, $region, $days, $sort, $offset, $search_id, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokSearchTheTiktokAdLibrary: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Keyword (ignored when advertiser_id is set) | [optional] [default to &#39;&#39;] |
| **advertiser_id** | **string**| Advertiser business id(s) for advertiser search | [optional] [default to &#39;&#39;] |
| **region** | **string**| EU region code (the Ad Library is EU-only) | [optional] [default to &#39;DE&#39;] |
| **days** | **int**|  | [optional] [default to 30] |
| **sort** | **string**|  | [optional] [default to &#39;last_shown_date,desc&#39;] |
| **offset** | **int**|  | [optional] [default to 0] |
| **search_id** | **string**|  | [optional] [default to &#39;&#39;] |
| **count** | **int**|  | [optional] [default to 20] |

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

## `tiktokSearchTiktokAdvertisers()`

```php
tiktokSearchTiktokAdvertisers($query, $region, $count): mixed
```

Search TikTok advertisers

Look up TikTok advertiser business ids by name (feeds ads/search?advertiser_id=).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Advertiser name (or partial) to look up
$region = 'DE'; // string | EU region code (the Ad Library is EU-only)
$count = 10; // int

try {
    $result = $apiInstance->tiktokSearchTiktokAdvertisers($query, $region, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokSearchTiktokAdvertisers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Advertiser name (or partial) to look up | |
| **region** | **string**| EU region code (the Ad Library is EU-only) | [optional] [default to &#39;DE&#39;] |
| **count** | **int**|  | [optional] [default to 10] |

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

## `tiktokSearchUsers()`

```php
tiktokSearchUsers($query, $region, $count, $cursor): mixed
```

Search users

Search TikTok users by keyword.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keyword
$region = 'US'; // string
$count = 20; // int
$cursor = 'cursor_example'; // string | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor

try {
    $result = $apiInstance->tiktokSearchUsers($query, $region, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokSearchUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keyword | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 20] |
| **cursor** | **string**| Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

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

## `tiktokSearchVideos()`

```php
tiktokSearchVideos($query, $region, $count, $cursor): mixed
```

Search videos

Search TikTok videos by keyword.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keyword
$region = 'US'; // string
$count = 20; // int
$cursor = 'cursor_example'; // string | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor

try {
    $result = $apiInstance->tiktokSearchVideos($query, $region, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokSearchVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keyword | |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 20] |
| **cursor** | **string**| Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

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

## `tiktokTrendingHashtags()`

```php
tiktokTrendingHashtags($region, $period, $count): mixed
```

Trending hashtags

Get trending hashtags (mobile Discover surface — view_count + creators).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$region = 'US'; // string
$period = 7; // int
$count = 20; // int

try {
    $result = $apiInstance->tiktokTrendingHashtags($region, $period, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokTrendingHashtags: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **period** | **int**|  | [optional] [default to 7] |
| **count** | **int**|  | [optional] [default to 20] |

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

## `tiktokTrendingSongs()`

```php
tiktokTrendingSongs($region, $period, $count): mixed
```

Trending songs

Get trending songs/sounds (mobile hot-music feed — ranked by usage).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$region = 'US'; // string
$period = 7; // int
$count = 20; // int

try {
    $result = $apiInstance->tiktokTrendingSongs($region, $period, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokTrendingSongs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **period** | **int**|  | [optional] [default to 7] |
| **count** | **int**|  | [optional] [default to 20] |

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

## `tiktokTrendingVideos()`

```php
tiktokTrendingVideos($region, $count): mixed
```

Trending videos

Get trending videos from the TikTok Explore feed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TikTokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$region = 'US'; // string
$count = 20; // int

try {
    $result = $apiInstance->tiktokTrendingVideos($region, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TikTokApi->tiktokTrendingVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **region** | **string**|  | [optional] [default to &#39;US&#39;] |
| **count** | **int**|  | [optional] [default to 20] |

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

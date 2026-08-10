# ScrapeBadger\RedditApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**redditGetCrossPosts()**](RedditApi.md#redditGetCrossPosts) | **GET** /v1/reddit/posts/{post_id}/duplicates | Get cross-posts |
| [**redditGetPostComments()**](RedditApi.md#redditGetPostComments) | **GET** /v1/reddit/posts/{post_id}/comments | Get post comments |
| [**redditGetPostDetail()**](RedditApi.md#redditGetPostDetail) | **GET** /v1/reddit/posts/{post_id} | Get post detail |
| [**redditGetPostsByDomain()**](RedditApi.md#redditGetPostsByDomain) | **GET** /v1/reddit/domains/{domain}/posts | Get posts by domain |
| [**redditGetSubredditInfo()**](RedditApi.md#redditGetSubredditInfo) | **GET** /v1/reddit/subreddits/{subreddit} | Get subreddit info |
| [**redditGetSubredditPosts()**](RedditApi.md#redditGetSubredditPosts) | **GET** /v1/reddit/subreddits/{subreddit}/posts | Get subreddit posts |
| [**redditGetSubredditRules()**](RedditApi.md#redditGetSubredditRules) | **GET** /v1/reddit/subreddits/{subreddit}/rules | Get subreddit rules |
| [**redditGetTrendingPosts()**](RedditApi.md#redditGetTrendingPosts) | **GET** /v1/reddit/posts/trending | Get trending posts |
| [**redditGetUserProfile()**](RedditApi.md#redditGetUserProfile) | **GET** /v1/reddit/users/{username} | Get user profile |
| [**redditGetUserSComments()**](RedditApi.md#redditGetUserSComments) | **GET** /v1/reddit/users/{username}/comments | Get user&#39;s comments |
| [**redditGetUserSModeratedSubreddits()**](RedditApi.md#redditGetUserSModeratedSubreddits) | **GET** /v1/reddit/users/{username}/moderated | Get user&#39;s moderated subreddits |
| [**redditGetUserSPosts()**](RedditApi.md#redditGetUserSPosts) | **GET** /v1/reddit/users/{username}/posts | Get user&#39;s posts |
| [**redditGetUserSTrophies()**](RedditApi.md#redditGetUserSTrophies) | **GET** /v1/reddit/users/{username}/trophies | Get user&#39;s trophies |
| [**redditGetWikiPageContent()**](RedditApi.md#redditGetWikiPageContent) | **GET** /v1/reddit/subreddits/{subreddit}/wiki/{page} | Get wiki page content |
| [**redditListWikiPages()**](RedditApi.md#redditListWikiPages) | **GET** /v1/reddit/subreddits/{subreddit}/wiki | List wiki pages |
| [**redditNewSubreddits()**](RedditApi.md#redditNewSubreddits) | **GET** /v1/reddit/subreddits/new | New subreddits |
| [**redditPopularSubreddits()**](RedditApi.md#redditPopularSubreddits) | **GET** /v1/reddit/subreddits/popular | Popular subreddits |
| [**redditRedditScraperHealthCheck()**](RedditApi.md#redditRedditScraperHealthCheck) | **GET** /v1/reddit/health | Reddit scraper health check |
| [**redditRedditScraperHealthCheckHead()**](RedditApi.md#redditRedditScraperHealthCheckHead) | **HEAD** /v1/reddit/health | Reddit scraper health check |
| [**redditSearchRedditPosts()**](RedditApi.md#redditSearchRedditPosts) | **GET** /v1/reddit/search/posts | Search Reddit posts |
| [**redditSearchSubreddits()**](RedditApi.md#redditSearchSubreddits) | **GET** /v1/reddit/search/subreddits | Search subreddits |
| [**redditSearchUsers()**](RedditApi.md#redditSearchUsers) | **GET** /v1/reddit/search/users | Search users |


## `redditGetCrossPosts()`

```php
redditGetCrossPosts($post_id, $limit, $after): mixed
```

Get cross-posts

Get cross-posts and duplicates of a Reddit post.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_id = 'post_id_example'; // string
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditGetCrossPosts($post_id, $limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetCrossPosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_id** | **string**|  | |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

## `redditGetPostComments()`

```php
redditGetPostComments($post_id, $sort, $limit, $depth): mixed
```

Get post comments

Get comment tree for a Reddit post.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_id = 'post_id_example'; // string
$sort = 'confidence'; // string | Sort: confidence, top, new, controversial, old, qa
$limit = 25; // int
$depth = 56; // int

try {
    $result = $apiInstance->redditGetPostComments($post_id, $sort, $limit, $depth);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetPostComments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_id** | **string**|  | |
| **sort** | **string**| Sort: confidence, top, new, controversial, old, qa | [optional] [default to &#39;confidence&#39;] |
| **limit** | **int**|  | [optional] [default to 25] |
| **depth** | **int**|  | [optional] |

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

## `redditGetPostDetail()`

```php
redditGetPostDetail($post_id): mixed
```

Get post detail

Get detailed information about a Reddit post.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_id = 'post_id_example'; // string

try {
    $result = $apiInstance->redditGetPostDetail($post_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetPostDetail: ', $e->getMessage(), PHP_EOL;
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

## `redditGetPostsByDomain()`

```php
redditGetPostsByDomain($domain, $sort, $t, $limit, $after): mixed
```

Get posts by domain

Get Reddit posts linking to a specific domain.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'domain_example'; // string
$sort = 'hot'; // string
$t = 'all'; // string
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditGetPostsByDomain($domain, $sort, $t, $limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetPostsByDomain: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**|  | |
| **sort** | **string**|  | [optional] [default to &#39;hot&#39;] |
| **t** | **string**|  | [optional] [default to &#39;all&#39;] |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

## `redditGetSubredditInfo()`

```php
redditGetSubredditInfo($subreddit): mixed
```

Get subreddit info

Get detailed information about a subreddit.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subreddit = 'subreddit_example'; // string

try {
    $result = $apiInstance->redditGetSubredditInfo($subreddit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetSubredditInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subreddit** | **string**|  | |

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

## `redditGetSubredditPosts()`

```php
redditGetSubredditPosts($subreddit, $sort, $t, $limit, $after): mixed
```

Get subreddit posts

Get posts from a subreddit with sorting options.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subreddit = 'subreddit_example'; // string
$sort = 'hot'; // string | Sort: hot, new, top, rising, controversial
$t = 'all'; // string | Time filter
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditGetSubredditPosts($subreddit, $sort, $t, $limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetSubredditPosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subreddit** | **string**|  | |
| **sort** | **string**| Sort: hot, new, top, rising, controversial | [optional] [default to &#39;hot&#39;] |
| **t** | **string**| Time filter | [optional] [default to &#39;all&#39;] |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

## `redditGetSubredditRules()`

```php
redditGetSubredditRules($subreddit): mixed
```

Get subreddit rules

Get the rules of a subreddit.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subreddit = 'subreddit_example'; // string

try {
    $result = $apiInstance->redditGetSubredditRules($subreddit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetSubredditRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subreddit** | **string**|  | |

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

## `redditGetTrendingPosts()`

```php
redditGetTrendingPosts($sort, $t, $limit, $after): mixed
```

Get trending posts

Get trending posts from Reddit's front page.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sort = 'hot'; // string | Sort: hot, new, top, rising, controversial, best
$t = 'day'; // string | Time filter
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditGetTrendingPosts($sort, $t, $limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetTrendingPosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sort** | **string**| Sort: hot, new, top, rising, controversial, best | [optional] [default to &#39;hot&#39;] |
| **t** | **string**| Time filter | [optional] [default to &#39;day&#39;] |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

## `redditGetUserProfile()`

```php
redditGetUserProfile($username): mixed
```

Get user profile

Get a Reddit user's profile.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string

try {
    $result = $apiInstance->redditGetUserProfile($username);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetUserProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |

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

## `redditGetUserSComments()`

```php
redditGetUserSComments($username, $sort, $t, $limit, $after): mixed
```

Get user's comments

Get comments by a Reddit user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$sort = 'new'; // string
$t = 'all'; // string
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditGetUserSComments($username, $sort, $t, $limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetUserSComments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **sort** | **string**|  | [optional] [default to &#39;new&#39;] |
| **t** | **string**|  | [optional] [default to &#39;all&#39;] |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

## `redditGetUserSModeratedSubreddits()`

```php
redditGetUserSModeratedSubreddits($username): mixed
```

Get user's moderated subreddits

Get subreddits moderated by a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string

try {
    $result = $apiInstance->redditGetUserSModeratedSubreddits($username);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetUserSModeratedSubreddits: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |

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

## `redditGetUserSPosts()`

```php
redditGetUserSPosts($username, $sort, $t, $limit, $after): mixed
```

Get user's posts

Get posts submitted by a Reddit user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$sort = 'new'; // string
$t = 'all'; // string
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditGetUserSPosts($username, $sort, $t, $limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetUserSPosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **sort** | **string**|  | [optional] [default to &#39;new&#39;] |
| **t** | **string**|  | [optional] [default to &#39;all&#39;] |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

## `redditGetUserSTrophies()`

```php
redditGetUserSTrophies($username): mixed
```

Get user's trophies

Get a user's trophy case.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string

try {
    $result = $apiInstance->redditGetUserSTrophies($username);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetUserSTrophies: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |

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

## `redditGetWikiPageContent()`

```php
redditGetWikiPageContent($subreddit, $page): mixed
```

Get wiki page content

Get the content of a specific wiki page.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subreddit = 'subreddit_example'; // string
$page = 'page_example'; // string

try {
    $result = $apiInstance->redditGetWikiPageContent($subreddit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditGetWikiPageContent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subreddit** | **string**|  | |
| **page** | **string**|  | |

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

## `redditListWikiPages()`

```php
redditListWikiPages($subreddit): mixed
```

List wiki pages

List all wiki pages in a subreddit.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subreddit = 'subreddit_example'; // string

try {
    $result = $apiInstance->redditListWikiPages($subreddit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditListWikiPages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subreddit** | **string**|  | |

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

## `redditNewSubreddits()`

```php
redditNewSubreddits($limit, $after): mixed
```

New subreddits

Get recently created subreddits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditNewSubreddits($limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditNewSubreddits: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

## `redditPopularSubreddits()`

```php
redditPopularSubreddits($limit, $after): mixed
```

Popular subreddits

Get popular subreddits by subscriber count.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditPopularSubreddits($limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditPopularSubreddits: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

## `redditRedditScraperHealthCheck()`

```php
redditRedditScraperHealthCheck(): mixed
```

Reddit scraper health check

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->redditRedditScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditRedditScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `redditRedditScraperHealthCheckHead()`

```php
redditRedditScraperHealthCheckHead(): mixed
```

Reddit scraper health check

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->redditRedditScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditRedditScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `redditSearchRedditPosts()`

```php
redditSearchRedditPosts($q, $subreddit, $sort, $t, $limit, $after): mixed
```

Search Reddit posts

Search Reddit posts globally or within a subreddit.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query
$subreddit = 'subreddit_example'; // string | Restrict to subreddit
$sort = 'relevance'; // string | Sort: relevance, hot, top, new, comments
$t = 'all'; // string | Time: hour, day, week, month, year, all
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditSearchRedditPosts($q, $subreddit, $sort, $t, $limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditSearchRedditPosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query | |
| **subreddit** | **string**| Restrict to subreddit | [optional] |
| **sort** | **string**| Sort: relevance, hot, top, new, comments | [optional] [default to &#39;relevance&#39;] |
| **t** | **string**| Time: hour, day, week, month, year, all | [optional] [default to &#39;all&#39;] |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

## `redditSearchSubreddits()`

```php
redditSearchSubreddits($q, $limit, $after): mixed
```

Search subreddits

Search for subreddits by keyword.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditSearchSubreddits($q, $limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditSearchSubreddits: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query | |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

## `redditSearchUsers()`

```php
redditSearchUsers($q, $limit, $after): mixed
```

Search users

Search for Reddit users.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query
$limit = 25; // int
$after = 'after_example'; // string

try {
    $result = $apiInstance->redditSearchUsers($q, $limit, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedditApi->redditSearchUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query | |
| **limit** | **int**|  | [optional] [default to 25] |
| **after** | **string**|  | [optional] |

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

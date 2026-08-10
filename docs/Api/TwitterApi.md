# ScrapeBadger\TwitterApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**twitterAdvancedTweetSearch()**](TwitterApi.md#twitterAdvancedTweetSearch) | **GET** /v1/twitter/tweets/advanced_search | Advanced tweet search |
| [**twitterBatchGetUsersByIds()**](TwitterApi.md#twitterBatchGetUsersByIds) | **GET** /v1/twitter/users/batch_by_ids | Batch get users by IDs |
| [**twitterBatchGetUsersByUsernames()**](TwitterApi.md#twitterBatchGetUsersByUsernames) | **GET** /v1/twitter/users/batch_by_usernames | Batch get users by usernames |
| [**twitterConfigureWebhookOnAMonitor()**](TwitterApi.md#twitterConfigureWebhookOnAMonitor) | **POST** /v1/twitter/stream/webhooks | Configure webhook on a monitor |
| [**twitterCreateFilterRule()**](TwitterApi.md#twitterCreateFilterRule) | **POST** /v1/twitter/stream/filter-rules | Create filter rule |
| [**twitterCreateStreamMonitor()**](TwitterApi.md#twitterCreateStreamMonitor) | **POST** /v1/twitter/stream/monitors | Create stream monitor |
| [**twitterDeleteFilterRule()**](TwitterApi.md#twitterDeleteFilterRule) | **DELETE** /v1/twitter/stream/filter-rules/{rule_id} | Delete filter rule |
| [**twitterDeleteStreamMonitor()**](TwitterApi.md#twitterDeleteStreamMonitor) | **DELETE** /v1/twitter/stream/monitors/{monitor_id} | Delete stream monitor |
| [**twitterGetArticleById()**](TwitterApi.md#twitterGetArticleById) | **GET** /v1/twitter/tweets/article/{article_id} | Get article by ID |
| [**twitterGetBroadcastDetails()**](TwitterApi.md#twitterGetBroadcastDetails) | **GET** /v1/twitter/spaces/broadcast/{broadcast_id} | Get broadcast details |
| [**twitterGetCommunityDetails()**](TwitterApi.md#twitterGetCommunityDetails) | **GET** /v1/twitter/communities/{community_id} | Get community details |
| [**twitterGetCommunityNotes()**](TwitterApi.md#twitterGetCommunityNotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/community_notes | Get community notes |
| [**twitterGetCommunityTweets()**](TwitterApi.md#twitterGetCommunityTweets) | **GET** /v1/twitter/communities/{community_id}/tweets | Get community tweets |
| [**twitterGetFilterRule()**](TwitterApi.md#twitterGetFilterRule) | **GET** /v1/twitter/stream/filter-rules/{rule_id} | Get filter rule |
| [**twitterGetFilterRulePerPollRates()**](TwitterApi.md#twitterGetFilterRulePerPollRates) | **GET** /v1/twitter/stream/filter-rules-pricing | Get filter rule per-poll rates |
| [**twitterGetListDetails()**](TwitterApi.md#twitterGetListDetails) | **GET** /v1/twitter/lists/{list_id}/detail | Get list details |
| [**twitterGetListTweets()**](TwitterApi.md#twitterGetListTweets) | **GET** /v1/twitter/lists/{list_id}/tweets | Get list tweets |
| [**twitterGetPlaceDetails()**](TwitterApi.md#twitterGetPlaceDetails) | **GET** /v1/twitter/geo/places/{place_id} | Get place details |
| [**twitterGetSimilarTweets()**](TwitterApi.md#twitterGetSimilarTweets) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/similar | Get similar tweets |
| [**twitterGetSpaceDetails()**](TwitterApi.md#twitterGetSpaceDetails) | **GET** /v1/twitter/spaces/{space_id} | Get Space details |
| [**twitterGetStreamMonitor()**](TwitterApi.md#twitterGetStreamMonitor) | **GET** /v1/twitter/stream/monitors/{monitor_id} | Get stream monitor |
| [**twitterGetTrendingTopics()**](TwitterApi.md#twitterGetTrendingTopics) | **GET** /v1/twitter/trends/ | Get trending topics |
| [**twitterGetTrendsByLocation()**](TwitterApi.md#twitterGetTrendsByLocation) | **GET** /v1/twitter/trends/place/{woeid} | Get trends by location |
| [**twitterGetTweetDetails()**](TwitterApi.md#twitterGetTweetDetails) | **GET** /v1/twitter/tweets/tweet/{tweet_id} | Get tweet details |
| [**twitterGetTweetEditHistory()**](TwitterApi.md#twitterGetTweetEditHistory) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/edit_history | Get tweet edit history |
| [**twitterGetTweetFavoriters()**](TwitterApi.md#twitterGetTweetFavoriters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/favoriters | Get tweet favoriters |
| [**twitterGetTweetQuotes()**](TwitterApi.md#twitterGetTweetQuotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/quotes | Get tweet quotes |
| [**twitterGetTweetReplies()**](TwitterApi.md#twitterGetTweetReplies) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/replies | Get tweet replies |
| [**twitterGetTweetRetweeters()**](TwitterApi.md#twitterGetTweetRetweeters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/retweeters | Get tweet retweeters |
| [**twitterGetTweetsByIds()**](TwitterApi.md#twitterGetTweetsByIds) | **GET** /v1/twitter/tweets/ | Get tweets by IDs |
| [**twitterGetUserArticles()**](TwitterApi.md#twitterGetUserArticles) | **GET** /v1/twitter/users/{user_id}/articles | Get user articles |
| [**twitterGetUserById()**](TwitterApi.md#twitterGetUserById) | **GET** /v1/twitter/users/{user_id}/by_id | Get user by ID |
| [**twitterGetUserByUsername()**](TwitterApi.md#twitterGetUserByUsername) | **GET** /v1/twitter/users/{username}/by_username | Get user by username |
| [**twitterGetUserFollowers()**](TwitterApi.md#twitterGetUserFollowers) | **GET** /v1/twitter/users/{username}/followers | Get user followers |
| [**twitterGetUserFollowing()**](TwitterApi.md#twitterGetUserFollowing) | **GET** /v1/twitter/users/{username}/followings | Get user following |
| [**twitterGetUserMentions()**](TwitterApi.md#twitterGetUserMentions) | **GET** /v1/twitter/users/{username}/mentions | Get user mentions |
| [**twitterGetUserSubscriptions()**](TwitterApi.md#twitterGetUserSubscriptions) | **GET** /v1/twitter/users/{user_id}/subscriptions | Get user subscriptions |
| [**twitterGetUserTweets()**](TwitterApi.md#twitterGetUserTweets) | **GET** /v1/twitter/users/{username}/latest_tweets | Get user tweets |
| [**twitterListBillingLogs()**](TwitterApi.md#twitterListBillingLogs) | **GET** /v1/twitter/stream/billing-logs | List billing logs |
| [**twitterListDeliveryLogsForAFilterRule()**](TwitterApi.md#twitterListDeliveryLogsForAFilterRule) | **GET** /v1/twitter/stream/filter-rules/{rule_id}/logs | List delivery logs for a filter rule |
| [**twitterListFilterRules()**](TwitterApi.md#twitterListFilterRules) | **GET** /v1/twitter/stream/filter-rules | List filter rules |
| [**twitterListStreamMonitors()**](TwitterApi.md#twitterListStreamMonitors) | **GET** /v1/twitter/stream/monitors | List stream monitors |
| [**twitterListTweetDeliveryLogs()**](TwitterApi.md#twitterListTweetDeliveryLogs) | **GET** /v1/twitter/stream/logs | List tweet delivery logs |
| [**twitterListWebhooks()**](TwitterApi.md#twitterListWebhooks) | **GET** /v1/twitter/stream/webhooks | List webhooks |
| [**twitterRemoveWebhookFromMonitor()**](TwitterApi.md#twitterRemoveWebhookFromMonitor) | **DELETE** /v1/twitter/stream/webhooks/{webhook_id} | Remove webhook from monitor |
| [**twitterSearchCommunities()**](TwitterApi.md#twitterSearchCommunities) | **GET** /v1/twitter/communities/search | Search communities |
| [**twitterSearchListTweets()**](TwitterApi.md#twitterSearchListTweets) | **GET** /v1/twitter/lists/{list_id}/search_tweets | Search list tweets |
| [**twitterSearchPlaces()**](TwitterApi.md#twitterSearchPlaces) | **GET** /v1/twitter/geo/search | Search places |
| [**twitterSearchUsers()**](TwitterApi.md#twitterSearchUsers) | **GET** /v1/twitter/users/search_users | Search users |
| [**twitterTestWebhookDelivery()**](TwitterApi.md#twitterTestWebhookDelivery) | **POST** /v1/twitter/stream/webhooks/test | Test webhook delivery |
| [**twitterTwitterScraperHealthCheck()**](TwitterApi.md#twitterTwitterScraperHealthCheck) | **GET** /v1/twitter/health | Twitter scraper health check |
| [**twitterTwitterScraperHealthCheckHead()**](TwitterApi.md#twitterTwitterScraperHealthCheckHead) | **HEAD** /v1/twitter/health | Twitter scraper health check |
| [**twitterUpdateFilterRule()**](TwitterApi.md#twitterUpdateFilterRule) | **PATCH** /v1/twitter/stream/filter-rules/{rule_id} | Update filter rule |
| [**twitterUpdateStreamMonitor()**](TwitterApi.md#twitterUpdateStreamMonitor) | **PATCH** /v1/twitter/stream/monitors/{monitor_id} | Update stream monitor |
| [**twitterValidateSearchQuery()**](TwitterApi.md#twitterValidateSearchQuery) | **POST** /v1/twitter/stream/filter-rules/validate | Validate search query |


## `twitterAdvancedTweetSearch()`

```php
twitterAdvancedTweetSearch($query, $query_type, $count, $cursor): mixed
```

Advanced tweet search

Search tweets with advanced options.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$query_type = 'query_type_example'; // string
$count = 56; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterAdvancedTweetSearch($query, $query_type, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterAdvancedTweetSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **query_type** | **string**|  | [optional] |
| **count** | **int**|  | [optional] |
| **cursor** | **string**|  | [optional] |

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

## `twitterBatchGetUsersByIds()`

```php
twitterBatchGetUsersByIds($user_ids): mixed
```

Batch get users by IDs

Get multiple user profiles by their numeric IDs (comma-separated).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_ids = 'user_ids_example'; // string

try {
    $result = $apiInstance->twitterBatchGetUsersByIds($user_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterBatchGetUsersByIds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_ids** | **string**|  | |

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

## `twitterBatchGetUsersByUsernames()`

```php
twitterBatchGetUsersByUsernames($usernames): mixed
```

Batch get users by usernames

Get multiple user profiles by their usernames (comma-separated).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$usernames = 'usernames_example'; // string

try {
    $result = $apiInstance->twitterBatchGetUsersByUsernames($usernames);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterBatchGetUsersByUsernames: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **usernames** | **string**|  | |

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

## `twitterConfigureWebhookOnAMonitor()`

```php
twitterConfigureWebhookOnAMonitor($webhook_create): \ScrapeBadger\Model\WebhookResponse
```

Configure webhook on a monitor

Configure a webhook delivery URL on a stream monitor.  The secret is returned only once on creation. Subsequent calls show secret_set: bool. If monitor already has a webhook, delete it first (409 is returned).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_create = new \ScrapeBadger\Model\WebhookCreate(); // \ScrapeBadger\Model\WebhookCreate

try {
    $result = $apiInstance->twitterConfigureWebhookOnAMonitor($webhook_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterConfigureWebhookOnAMonitor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_create** | [**\ScrapeBadger\Model\WebhookCreate**](../Model/WebhookCreate.md)|  | |

### Return type

[**\ScrapeBadger\Model\WebhookResponse**](../Model/WebhookResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterCreateFilterRule()`

```php
twitterCreateFilterRule($filter_rule_create): \ScrapeBadger\Model\FilterRuleResponse
```

Create filter rule

Create a new query-based tweet filter rule.  The rule starts in 'active' status immediately. Credits must be positive. The (api_key_id, tag) pair must be unique.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$filter_rule_create = new \ScrapeBadger\Model\FilterRuleCreate(); // \ScrapeBadger\Model\FilterRuleCreate

try {
    $result = $apiInstance->twitterCreateFilterRule($filter_rule_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterCreateFilterRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **filter_rule_create** | [**\ScrapeBadger\Model\FilterRuleCreate**](../Model/FilterRuleCreate.md)|  | |

### Return type

[**\ScrapeBadger\Model\FilterRuleResponse**](../Model/FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterCreateStreamMonitor()`

```php
twitterCreateStreamMonitor($stream_monitor_create): \ScrapeBadger\Model\StreamMonitorResponse
```

Create stream monitor

Create a new stream monitor to watch Twitter accounts in real-time.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$stream_monitor_create = new \ScrapeBadger\Model\StreamMonitorCreate(); // \ScrapeBadger\Model\StreamMonitorCreate

try {
    $result = $apiInstance->twitterCreateStreamMonitor($stream_monitor_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterCreateStreamMonitor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **stream_monitor_create** | [**\ScrapeBadger\Model\StreamMonitorCreate**](../Model/StreamMonitorCreate.md)|  | |

### Return type

[**\ScrapeBadger\Model\StreamMonitorResponse**](../Model/StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterDeleteFilterRule()`

```php
twitterDeleteFilterRule($rule_id)
```

Delete filter rule

Delete a filter rule and all its logs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rule_id = 'rule_id_example'; // string

try {
    $apiInstance->twitterDeleteFilterRule($rule_id);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterDeleteFilterRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rule_id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterDeleteStreamMonitor()`

```php
twitterDeleteStreamMonitor($monitor_id)
```

Delete stream monitor

Delete a stream monitor and all its logs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$monitor_id = 'monitor_id_example'; // string

try {
    $apiInstance->twitterDeleteStreamMonitor($monitor_id);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterDeleteStreamMonitor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **monitor_id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterGetArticleById()`

```php
twitterGetArticleById($article_id): mixed
```

Get article by ID

Get a long-form article by its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$article_id = 'article_id_example'; // string

try {
    $result = $apiInstance->twitterGetArticleById($article_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetArticleById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **article_id** | **string**|  | |

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

## `twitterGetBroadcastDetails()`

```php
twitterGetBroadcastDetails($broadcast_id): mixed
```

Get broadcast details

Get details of a live video broadcast.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$broadcast_id = 'broadcast_id_example'; // string

try {
    $result = $apiInstance->twitterGetBroadcastDetails($broadcast_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetBroadcastDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **broadcast_id** | **string**|  | |

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

## `twitterGetCommunityDetails()`

```php
twitterGetCommunityDetails($community_id): mixed
```

Get community details

Get details of a specific community.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$community_id = 'community_id_example'; // string

try {
    $result = $apiInstance->twitterGetCommunityDetails($community_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetCommunityDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_id** | **string**|  | |

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

## `twitterGetCommunityNotes()`

```php
twitterGetCommunityNotes($tweet_id): mixed
```

Get community notes

Get community notes (Birdwatch) for a specific tweet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tweet_id = 'tweet_id_example'; // string

try {
    $result = $apiInstance->twitterGetCommunityNotes($tweet_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetCommunityNotes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tweet_id** | **string**|  | |

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

## `twitterGetCommunityTweets()`

```php
twitterGetCommunityTweets($community_id, $tweet_type, $cursor): mixed
```

Get community tweets

Get tweets from a specific community.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$community_id = 'community_id_example'; // string
$tweet_type = 'tweet_type_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetCommunityTweets($community_id, $tweet_type, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetCommunityTweets: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_id** | **string**|  | |
| **tweet_type** | **string**|  | [optional] |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetFilterRule()`

```php
twitterGetFilterRule($rule_id): \ScrapeBadger\Model\FilterRuleResponse
```

Get filter rule

Get a single filter rule by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rule_id = 'rule_id_example'; // string

try {
    $result = $apiInstance->twitterGetFilterRule($rule_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetFilterRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rule_id** | **string**|  | |

### Return type

[**\ScrapeBadger\Model\FilterRuleResponse**](../Model/FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterGetFilterRulePerPollRates()`

```php
twitterGetFilterRulePerPollRates(): \ScrapeBadger\Model\PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse
```

Get filter rule per-poll rates

Current per-poll rates (auth required — used by SDK + dashboard).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->twitterGetFilterRulePerPollRates();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetFilterRulePerPollRates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ScrapeBadger\Model\PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse**](../Model/PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterGetListDetails()`

```php
twitterGetListDetails($list_id): mixed
```

Get list details

Get details of a specific list.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$list_id = 'list_id_example'; // string

try {
    $result = $apiInstance->twitterGetListDetails($list_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetListDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **list_id** | **string**|  | |

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

## `twitterGetListTweets()`

```php
twitterGetListTweets($list_id, $cursor): mixed
```

Get list tweets

Get tweets from a specific list.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$list_id = 'list_id_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetListTweets($list_id, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetListTweets: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **list_id** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetPlaceDetails()`

```php
twitterGetPlaceDetails($place_id): mixed
```

Get place details

Get details of a specific place.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$place_id = 'place_id_example'; // string

try {
    $result = $apiInstance->twitterGetPlaceDetails($place_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetPlaceDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **place_id** | **string**|  | |

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

## `twitterGetSimilarTweets()`

```php
twitterGetSimilarTweets($tweet_id): mixed
```

Get similar tweets

Get tweets similar to a specific tweet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tweet_id = 'tweet_id_example'; // string

try {
    $result = $apiInstance->twitterGetSimilarTweets($tweet_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetSimilarTweets: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tweet_id** | **string**|  | |

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

## `twitterGetSpaceDetails()`

```php
twitterGetSpaceDetails($space_id): mixed
```

Get Space details

Get details of a Twitter Space.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$space_id = 'space_id_example'; // string

try {
    $result = $apiInstance->twitterGetSpaceDetails($space_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetSpaceDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **space_id** | **string**|  | |

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

## `twitterGetStreamMonitor()`

```php
twitterGetStreamMonitor($monitor_id): \ScrapeBadger\Model\StreamMonitorResponse
```

Get stream monitor

Get a single stream monitor by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$monitor_id = 'monitor_id_example'; // string

try {
    $result = $apiInstance->twitterGetStreamMonitor($monitor_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetStreamMonitor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **monitor_id** | **string**|  | |

### Return type

[**\ScrapeBadger\Model\StreamMonitorResponse**](../Model/StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterGetTrendingTopics()`

```php
twitterGetTrendingTopics($category, $count): mixed
```

Get trending topics

Get trending topics.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category = 'category_example'; // string
$count = 56; // int

try {
    $result = $apiInstance->twitterGetTrendingTopics($category, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetTrendingTopics: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category** | **string**|  | [optional] |
| **count** | **int**|  | [optional] |

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

## `twitterGetTrendsByLocation()`

```php
twitterGetTrendsByLocation($woeid): mixed
```

Get trends by location

Get trending topics for a specific location (WOEID).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$woeid = 'woeid_example'; // string

try {
    $result = $apiInstance->twitterGetTrendsByLocation($woeid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetTrendsByLocation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **woeid** | **string**|  | |

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

## `twitterGetTweetDetails()`

```php
twitterGetTweetDetails($tweet_id, $cursor): mixed
```

Get tweet details

Get detailed information about a specific tweet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tweet_id = 'tweet_id_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetTweetDetails($tweet_id, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetTweetDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tweet_id** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetTweetEditHistory()`

```php
twitterGetTweetEditHistory($tweet_id): mixed
```

Get tweet edit history

Get the edit history of a tweet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tweet_id = 'tweet_id_example'; // string

try {
    $result = $apiInstance->twitterGetTweetEditHistory($tweet_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetTweetEditHistory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tweet_id** | **string**|  | |

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

## `twitterGetTweetFavoriters()`

```php
twitterGetTweetFavoriters($tweet_id, $cursor): mixed
```

Get tweet favoriters

Get users who favorited a specific tweet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tweet_id = 'tweet_id_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetTweetFavoriters($tweet_id, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetTweetFavoriters: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tweet_id** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetTweetQuotes()`

```php
twitterGetTweetQuotes($tweet_id, $cursor): mixed
```

Get tweet quotes

Get tweets that quote a specific tweet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tweet_id = 'tweet_id_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetTweetQuotes($tweet_id, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetTweetQuotes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tweet_id** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetTweetReplies()`

```php
twitterGetTweetReplies($tweet_id, $cursor): mixed
```

Get tweet replies

Get replies to a specific tweet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tweet_id = 'tweet_id_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetTweetReplies($tweet_id, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetTweetReplies: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tweet_id** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetTweetRetweeters()`

```php
twitterGetTweetRetweeters($tweet_id, $cursor): mixed
```

Get tweet retweeters

Get users who retweeted a specific tweet.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tweet_id = 'tweet_id_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetTweetRetweeters($tweet_id, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetTweetRetweeters: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tweet_id** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetTweetsByIds()`

```php
twitterGetTweetsByIds($tweets): mixed
```

Get tweets by IDs

Get multiple tweets by their IDs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tweets = 'tweets_example'; // string

try {
    $result = $apiInstance->twitterGetTweetsByIds($tweets);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetTweetsByIds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tweets** | **string**|  | |

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

## `twitterGetUserArticles()`

```php
twitterGetUserArticles($user_id, $cursor): mixed
```

Get user articles

Get long-form articles written by a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetUserArticles($user_id, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetUserArticles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetUserById()`

```php
twitterGetUserById($user_id): mixed
```

Get user by ID

Get user profile by user ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string

try {
    $result = $apiInstance->twitterGetUserById($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetUserById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**|  | |

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

## `twitterGetUserByUsername()`

```php
twitterGetUserByUsername($username): mixed
```

Get user by username

Get user profile by username.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string

try {
    $result = $apiInstance->twitterGetUserByUsername($username);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetUserByUsername: ', $e->getMessage(), PHP_EOL;
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

## `twitterGetUserFollowers()`

```php
twitterGetUserFollowers($username, $cursor): mixed
```

Get user followers

Get followers of a specific user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetUserFollowers($username, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetUserFollowers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetUserFollowing()`

```php
twitterGetUserFollowing($username, $cursor): mixed
```

Get user following

Get users that a specific user is following.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetUserFollowing($username, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetUserFollowing: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetUserMentions()`

```php
twitterGetUserMentions($username, $count, $cursor): mixed
```

Get user mentions

Get tweets mentioning a specific user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$count = 56; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetUserMentions($username, $count, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetUserMentions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **count** | **int**|  | [optional] |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetUserSubscriptions()`

```php
twitterGetUserSubscriptions($user_id, $cursor): mixed
```

Get user subscriptions

Get subscriptions of a specific user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetUserSubscriptions($user_id, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetUserSubscriptions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterGetUserTweets()`

```php
twitterGetUserTweets($username, $cursor): mixed
```

Get user tweets

Get latest tweets from a specific user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterGetUserTweets($username, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterGetUserTweets: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterListBillingLogs()`

```php
twitterListBillingLogs($monitor_id, $page, $page_size): \ScrapeBadger\Model\BillingLogListResponse
```

List billing logs

List billing activity logs for the authenticated API key's monitors.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$monitor_id = 'monitor_id_example'; // string
$page = 1; // int
$page_size = 20; // int

try {
    $result = $apiInstance->twitterListBillingLogs($monitor_id, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterListBillingLogs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **monitor_id** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 20] |

### Return type

[**\ScrapeBadger\Model\BillingLogListResponse**](../Model/BillingLogListResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterListDeliveryLogsForAFilterRule()`

```php
twitterListDeliveryLogsForAFilterRule($rule_id, $delivery_status, $author_username, $page, $page_size, $sort): \ScrapeBadger\Model\FilterRuleDeliveryLogListResponse
```

List delivery logs for a filter rule

List tweet delivery logs for a specific filter rule.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rule_id = 'rule_id_example'; // string
$delivery_status = 'delivery_status_example'; // string
$author_username = 'author_username_example'; // string
$page = 1; // int
$page_size = 20; // int
$sort = 'desc'; // string

try {
    $result = $apiInstance->twitterListDeliveryLogsForAFilterRule($rule_id, $delivery_status, $author_username, $page, $page_size, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterListDeliveryLogsForAFilterRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rule_id** | **string**|  | |
| **delivery_status** | **string**|  | [optional] |
| **author_username** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 20] |
| **sort** | **string**|  | [optional] [default to &#39;desc&#39;] |

### Return type

[**\ScrapeBadger\Model\FilterRuleDeliveryLogListResponse**](../Model/FilterRuleDeliveryLogListResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterListFilterRules()`

```php
twitterListFilterRules($status, $page, $page_size): \ScrapeBadger\Model\FilterRuleListResponse
```

List filter rules

List all filter rules for the authenticated API key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$status = 'status_example'; // string
$page = 1; // int
$page_size = 20; // int

try {
    $result = $apiInstance->twitterListFilterRules($status, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterListFilterRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 20] |

### Return type

[**\ScrapeBadger\Model\FilterRuleListResponse**](../Model/FilterRuleListResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterListStreamMonitors()`

```php
twitterListStreamMonitors($status, $page, $page_size): \ScrapeBadger\Model\StreamMonitorListResponse
```

List stream monitors

List all stream monitors for the authenticated API key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$status = 'status_example'; // string
$page = 1; // int
$page_size = 20; // int

try {
    $result = $apiInstance->twitterListStreamMonitors($status, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterListStreamMonitors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 20] |

### Return type

[**\ScrapeBadger\Model\StreamMonitorListResponse**](../Model/StreamMonitorListResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterListTweetDeliveryLogs()`

```php
twitterListTweetDeliveryLogs($monitor_id, $author_username, $delivery_status, $page, $page_size, $sort): \ScrapeBadger\Model\TweetDeliveryLogListResponse
```

List tweet delivery logs

List tweet delivery logs for the authenticated API key's monitors.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$monitor_id = 'monitor_id_example'; // string
$author_username = 'author_username_example'; // string
$delivery_status = 'delivery_status_example'; // string
$page = 1; // int
$page_size = 20; // int
$sort = 'desc'; // string

try {
    $result = $apiInstance->twitterListTweetDeliveryLogs($monitor_id, $author_username, $delivery_status, $page, $page_size, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterListTweetDeliveryLogs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **monitor_id** | **string**|  | [optional] |
| **author_username** | **string**|  | [optional] |
| **delivery_status** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 20] |
| **sort** | **string**|  | [optional] [default to &#39;desc&#39;] |

### Return type

[**\ScrapeBadger\Model\TweetDeliveryLogListResponse**](../Model/TweetDeliveryLogListResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterListWebhooks()`

```php
twitterListWebhooks($monitor_id): \ScrapeBadger\Model\WebhookListResponse
```

List webhooks

List all webhook-configured monitors for the authenticated API key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$monitor_id = 'monitor_id_example'; // string

try {
    $result = $apiInstance->twitterListWebhooks($monitor_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterListWebhooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **monitor_id** | **string**|  | [optional] |

### Return type

[**\ScrapeBadger\Model\WebhookListResponse**](../Model/WebhookListResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterRemoveWebhookFromMonitor()`

```php
twitterRemoveWebhookFromMonitor($webhook_id)
```

Remove webhook from monitor

Remove webhook configuration from a monitor. webhook_id is the monitor_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_id = 'webhook_id_example'; // string

try {
    $apiInstance->twitterRemoveWebhookFromMonitor($webhook_id);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterRemoveWebhookFromMonitor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterSearchCommunities()`

```php
twitterSearchCommunities($query, $cursor): mixed
```

Search communities

Search for communities by query.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterSearchCommunities($query, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterSearchCommunities: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterSearchListTweets()`

```php
twitterSearchListTweets($list_id, $query, $cursor): mixed
```

Search list tweets

Search tweets within a specific list.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$list_id = 'list_id_example'; // string
$query = 'query_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterSearchListTweets($list_id, $query, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterSearchListTweets: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **list_id** | **string**|  | |
| **query** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterSearchPlaces()`

```php
twitterSearchPlaces($query, $lat, $long): mixed
```

Search places

Search for places by query or coordinates.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$lat = 3.4; // float
$long = 3.4; // float

try {
    $result = $apiInstance->twitterSearchPlaces($query, $lat, $long);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterSearchPlaces: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | [optional] |
| **lat** | **float**|  | [optional] |
| **long** | **float**|  | [optional] |

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

## `twitterSearchUsers()`

```php
twitterSearchUsers($query, $cursor): mixed
```

Search users

Search for users by query.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->twitterSearchUsers($query, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterSearchUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **cursor** | **string**|  | [optional] |

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

## `twitterTestWebhookDelivery()`

```php
twitterTestWebhookDelivery($webhook_test_request): \ScrapeBadger\Model\WebhookTestResponse
```

Test webhook delivery

Send a test payload to a monitor's webhook URL.  The test payload has type=\"test\" instead of type=\"tweet\". Makes a synchronous HTTP POST and returns the delivery result.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_test_request = new \ScrapeBadger\Model\WebhookTestRequest(); // \ScrapeBadger\Model\WebhookTestRequest

try {
    $result = $apiInstance->twitterTestWebhookDelivery($webhook_test_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterTestWebhookDelivery: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_test_request** | [**\ScrapeBadger\Model\WebhookTestRequest**](../Model/WebhookTestRequest.md)|  | |

### Return type

[**\ScrapeBadger\Model\WebhookTestResponse**](../Model/WebhookTestResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterTwitterScraperHealthCheck()`

```php
twitterTwitterScraperHealthCheck(): mixed
```

Twitter scraper health check

Check health of the Twitter scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->twitterTwitterScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterTwitterScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `twitterTwitterScraperHealthCheckHead()`

```php
twitterTwitterScraperHealthCheckHead(): mixed
```

Twitter scraper health check

Check health of the Twitter scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->twitterTwitterScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterTwitterScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `twitterUpdateFilterRule()`

```php
twitterUpdateFilterRule($rule_id, $filter_rule_update): \ScrapeBadger\Model\FilterRuleResponse
```

Update filter rule

Partially update a filter rule.  Setting status='active' on a paused rule performs a credit check.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rule_id = 'rule_id_example'; // string
$filter_rule_update = new \ScrapeBadger\Model\FilterRuleUpdate(); // \ScrapeBadger\Model\FilterRuleUpdate

try {
    $result = $apiInstance->twitterUpdateFilterRule($rule_id, $filter_rule_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterUpdateFilterRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rule_id** | **string**|  | |
| **filter_rule_update** | [**\ScrapeBadger\Model\FilterRuleUpdate**](../Model/FilterRuleUpdate.md)|  | |

### Return type

[**\ScrapeBadger\Model\FilterRuleResponse**](../Model/FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterUpdateStreamMonitor()`

```php
twitterUpdateStreamMonitor($monitor_id, $stream_monitor_update): \ScrapeBadger\Model\StreamMonitorResponse
```

Update stream monitor

Partially update a stream monitor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$monitor_id = 'monitor_id_example'; // string
$stream_monitor_update = new \ScrapeBadger\Model\StreamMonitorUpdate(); // \ScrapeBadger\Model\StreamMonitorUpdate

try {
    $result = $apiInstance->twitterUpdateStreamMonitor($monitor_id, $stream_monitor_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterUpdateStreamMonitor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **monitor_id** | **string**|  | |
| **stream_monitor_update** | [**\ScrapeBadger\Model\StreamMonitorUpdate**](../Model/StreamMonitorUpdate.md)|  | |

### Return type

[**\ScrapeBadger\Model\StreamMonitorResponse**](../Model/StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `twitterValidateSearchQuery()`

```php
twitterValidateSearchQuery($filter_rule_validate_request): \ScrapeBadger\Model\FilterRuleValidateResponse
```

Validate search query

Validate a Twitter search query string.  Performs basic structural validation without making a live Twitter request. Returns valid=True if the query passes syntax checks.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TwitterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$filter_rule_validate_request = new \ScrapeBadger\Model\FilterRuleValidateRequest(); // \ScrapeBadger\Model\FilterRuleValidateRequest

try {
    $result = $apiInstance->twitterValidateSearchQuery($filter_rule_validate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TwitterApi->twitterValidateSearchQuery: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **filter_rule_validate_request** | [**\ScrapeBadger\Model\FilterRuleValidateRequest**](../Model/FilterRuleValidateRequest.md)|  | |

### Return type

[**\ScrapeBadger\Model\FilterRuleValidateResponse**](../Model/FilterRuleValidateResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

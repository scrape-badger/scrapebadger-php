# ScrapeBadger\BaiduApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**baiduBaiduImageSearch()**](BaiduApi.md#baiduBaiduImageSearch) | **GET** /v1/baidu/images | Baidu image search |
| [**baiduBaiduNewsSearch()**](BaiduApi.md#baiduBaiduNewsSearch) | **GET** /v1/baidu/news | Baidu news search |
| [**baiduBaiduScraperHealthCheck()**](BaiduApi.md#baiduBaiduScraperHealthCheck) | **GET** /v1/baidu/health | Baidu scraper health check |
| [**baiduBaiduScraperHealthCheckHead()**](BaiduApi.md#baiduBaiduScraperHealthCheckHead) | **HEAD** /v1/baidu/health | Baidu scraper health check |
| [**baiduBaiduWebSearch()**](BaiduApi.md#baiduBaiduWebSearch) | **GET** /v1/baidu/search | Baidu web search |
| [**baiduSearchSuggestions()**](BaiduApi.md#baiduSearchSuggestions) | **GET** /v1/baidu/autocomplete | Search suggestions |


## `baiduBaiduImageSearch()`

```php
baiduBaiduImageSearch($query, $page): mixed
```

Baidu image search

Baidu image search via the acjson JSON API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BaiduApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords
$page = 1; // int | 30 images per page

try {
    $result = $apiInstance->baiduBaiduImageSearch($query, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BaiduApi->baiduBaiduImageSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords | |
| **page** | **int**| 30 images per page | [optional] [default to 1] |

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

## `baiduBaiduNewsSearch()`

```php
baiduBaiduNewsSearch($query, $page): mixed
```

Baidu news search

Baidu news vertical — articles with source, publish date and real URLs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BaiduApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords
$page = 1; // int

try {
    $result = $apiInstance->baiduBaiduNewsSearch($query, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BaiduApi->baiduBaiduNewsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords | |
| **page** | **int**|  | [optional] [default to 1] |

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

## `baiduBaiduScraperHealthCheck()`

```php
baiduBaiduScraperHealthCheck(): mixed
```

Baidu scraper health check

Check health of the Baidu scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BaiduApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->baiduBaiduScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BaiduApi->baiduBaiduScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `baiduBaiduScraperHealthCheckHead()`

```php
baiduBaiduScraperHealthCheckHead(): mixed
```

Baidu scraper health check

Check health of the Baidu scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BaiduApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->baiduBaiduScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BaiduApi->baiduBaiduScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `baiduBaiduWebSearch()`

```php
baiduBaiduWebSearch($query, $page, $num): mixed
```

Baidu web search

Baidu web SERP — organic results with real target URLs, related searches, total count.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BaiduApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. '咖啡机' or 'coffee machine'
$page = 1; // int | Result page (10 results per page)
$num = 10; // int | Results per page (rn)

try {
    $result = $apiInstance->baiduBaiduWebSearch($query, $page, $num);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BaiduApi->baiduBaiduWebSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;咖啡机&#39; or &#39;coffee machine&#39; | |
| **page** | **int**| Result page (10 results per page) | [optional] [default to 1] |
| **num** | **int**| Results per page (rn) | [optional] [default to 10] |

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

## `baiduSearchSuggestions()`

```php
baiduSearchSuggestions($query): mixed
```

Search suggestions

Baidu search-box suggestions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BaiduApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial search term, e.g. '咖啡' or 'coff'

try {
    $result = $apiInstance->baiduSearchSuggestions($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BaiduApi->baiduSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial search term, e.g. &#39;咖啡&#39; or &#39;coff&#39; | |

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

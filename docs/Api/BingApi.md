# ScrapeBadger\BingApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bingBingScraperHealthCheck()**](BingApi.md#bingBingScraperHealthCheck) | **GET** /v1/bing/health | Bing scraper health check |
| [**bingBingScraperHealthCheckHead()**](BingApi.md#bingBingScraperHealthCheckHead) | **HEAD** /v1/bing/health | Bing scraper health check |
| [**bingImageSearch()**](BingApi.md#bingImageSearch) | **GET** /v1/bing/images | Image search |
| [**bingListSupportedMarkets()**](BingApi.md#bingListSupportedMarkets) | **GET** /v1/bing/markets | List supported markets |
| [**bingNewsSearch()**](BingApi.md#bingNewsSearch) | **GET** /v1/bing/news | News search |
| [**bingSearchSuggestions()**](BingApi.md#bingSearchSuggestions) | **GET** /v1/bing/autocomplete | Search suggestions |
| [**bingVideoSearch()**](BingApi.md#bingVideoSearch) | **GET** /v1/bing/videos | Video search |
| [**bingWebSearch()**](BingApi.md#bingWebSearch) | **GET** /v1/bing/search | Web search |


## `bingBingScraperHealthCheck()`

```php
bingBingScraperHealthCheck(): mixed
```

Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->bingBingScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BingApi->bingBingScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `bingBingScraperHealthCheckHead()`

```php
bingBingScraperHealthCheckHead(): mixed
```

Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->bingBingScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BingApi->bingBingScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `bingImageSearch()`

```php
bingImageSearch($query, $market, $count, $safe_search): mixed
```

Image search

Bing Images — thumbnail, full-size and source URL per result.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'golden retriever'
$market = 'en-US'; // string | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
$count = 35; // int | Results to return
$safe_search = 'safe_search_example'; // string | off | moderate | strict

try {
    $result = $apiInstance->bingImageSearch($query, $market, $count, $safe_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BingApi->bingImageSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;golden retriever&#39; | |
| **market** | **string**| Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &#39;en-US&#39;] |
| **count** | **int**| Results to return | [optional] [default to 35] |
| **safe_search** | **string**| off | moderate | strict | [optional] |

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

## `bingListSupportedMarkets()`

```php
bingListSupportedMarkets(): mixed
```

List supported markets

Supported Bing market codes. Free — costs no credits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->bingListSupportedMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BingApi->bingListSupportedMarkets: ', $e->getMessage(), PHP_EOL;
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

## `bingNewsSearch()`

```php
bingNewsSearch($query, $market, $freshness): mixed
```

News search

Bing News — headline, source, published time and snippet per article.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'interest rates'
$market = 'en-US'; // string | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
$freshness = 'freshness_example'; // string | day | week | month — restrict to recent articles

try {
    $result = $apiInstance->bingNewsSearch($query, $market, $freshness);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BingApi->bingNewsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;interest rates&#39; | |
| **market** | **string**| Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &#39;en-US&#39;] |
| **freshness** | **string**| day | week | month — restrict to recent articles | [optional] |

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

## `bingSearchSuggestions()`

```php
bingSearchSuggestions($query, $market): mixed
```

Search suggestions

Bing search-box query suggestions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial search term, e.g. 'coff'
$market = 'en-US'; // string | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.

try {
    $result = $apiInstance->bingSearchSuggestions($query, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BingApi->bingSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial search term, e.g. &#39;coff&#39; | |
| **market** | **string**| Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &#39;en-US&#39;] |

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

## `bingVideoSearch()`

```php
bingVideoSearch($query, $market, $count, $safe_search): mixed
```

Video search

Bing Videos — title, thumbnail, duration, publisher and source per result.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'espresso tutorial'
$market = 'en-US'; // string | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
$count = 35; // int | Results to return
$safe_search = 'safe_search_example'; // string | off | moderate | strict

try {
    $result = $apiInstance->bingVideoSearch($query, $market, $count, $safe_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BingApi->bingVideoSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;espresso tutorial&#39; | |
| **market** | **string**| Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &#39;en-US&#39;] |
| **count** | **int**| Results to return | [optional] [default to 35] |
| **safe_search** | **string**| off | moderate | strict | [optional] |

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

## `bingWebSearch()`

```php
bingWebSearch($query, $market, $count, $offset, $safe_search): mixed
```

Web search

Bing web SERP — organic results, ads, related searches and total count.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'coffee machine'
$market = 'en-US'; // string | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
$count = 10; // int | Results per page (1-50)
$offset = 0; // int | Zero-based result offset for pagination
$safe_search = 'safe_search_example'; // string | off | moderate | strict (default moderate)

try {
    $result = $apiInstance->bingWebSearch($query, $market, $count, $offset, $safe_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BingApi->bingWebSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;coffee machine&#39; | |
| **market** | **string**| Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &#39;en-US&#39;] |
| **count** | **int**| Results per page (1-50) | [optional] [default to 10] |
| **offset** | **int**| Zero-based result offset for pagination | [optional] [default to 0] |
| **safe_search** | **string**| off | moderate | strict (default moderate) | [optional] |

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

# ScrapeBadger\YahooApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**yahooImageSearch()**](YahooApi.md#yahooImageSearch) | **GET** /v1/yahoo/images | Image search |
| [**yahooListSupportedMarkets()**](YahooApi.md#yahooListSupportedMarkets) | **GET** /v1/yahoo/markets | List supported markets |
| [**yahooNewsSearch()**](YahooApi.md#yahooNewsSearch) | **GET** /v1/yahoo/news | News search |
| [**yahooSearchSuggestions()**](YahooApi.md#yahooSearchSuggestions) | **GET** /v1/yahoo/autocomplete | Search suggestions |
| [**yahooVideoSearch()**](YahooApi.md#yahooVideoSearch) | **GET** /v1/yahoo/videos | Video search |
| [**yahooWebSearch()**](YahooApi.md#yahooWebSearch) | **GET** /v1/yahoo/search | Web search |
| [**yahooYahooScraperHealthCheck()**](YahooApi.md#yahooYahooScraperHealthCheck) | **GET** /v1/yahoo/health | Yahoo scraper health check |
| [**yahooYahooScraperHealthCheckHead()**](YahooApi.md#yahooYahooScraperHealthCheckHead) | **HEAD** /v1/yahoo/health | Yahoo scraper health check |


## `yahooImageSearch()`

```php
yahooImageSearch($query, $market, $count): mixed
```

Image search

Yahoo Images — thumbnail, full-size and source URL per result.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YahooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'golden retriever'
$market = 'us'; // string | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
$count = 30; // int | Results to return

try {
    $result = $apiInstance->yahooImageSearch($query, $market, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YahooApi->yahooImageSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;golden retriever&#39; | |
| **market** | **string**| Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &#39;us&#39;] |
| **count** | **int**| Results to return | [optional] [default to 30] |

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

## `yahooListSupportedMarkets()`

```php
yahooListSupportedMarkets(): mixed
```

List supported markets

Supported Yahoo market codes. Free — costs no credits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YahooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->yahooListSupportedMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YahooApi->yahooListSupportedMarkets: ', $e->getMessage(), PHP_EOL;
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

## `yahooNewsSearch()`

```php
yahooNewsSearch($query, $market): mixed
```

News search

Yahoo News — headline, source, published time and snippet per article.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YahooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'interest rates'
$market = 'us'; // string | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.

try {
    $result = $apiInstance->yahooNewsSearch($query, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YahooApi->yahooNewsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;interest rates&#39; | |
| **market** | **string**| Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &#39;us&#39;] |

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

## `yahooSearchSuggestions()`

```php
yahooSearchSuggestions($query, $market): mixed
```

Search suggestions

Yahoo search-box query suggestions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YahooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial search term, e.g. 'coff'
$market = 'us'; // string | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.

try {
    $result = $apiInstance->yahooSearchSuggestions($query, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YahooApi->yahooSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial search term, e.g. &#39;coff&#39; | |
| **market** | **string**| Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &#39;us&#39;] |

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

## `yahooVideoSearch()`

```php
yahooVideoSearch($query, $market, $count): mixed
```

Video search

Yahoo Videos — title, thumbnail, duration, publisher and source per result.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YahooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'espresso tutorial'
$market = 'us'; // string | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
$count = 30; // int | Results to return

try {
    $result = $apiInstance->yahooVideoSearch($query, $market, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YahooApi->yahooVideoSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;espresso tutorial&#39; | |
| **market** | **string**| Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &#39;us&#39;] |
| **count** | **int**| Results to return | [optional] [default to 30] |

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

## `yahooWebSearch()`

```php
yahooWebSearch($query, $market, $offset, $safe_search): mixed
```

Web search

Yahoo web SERP — organic results, ads, related searches and total count.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YahooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'coffee machine'
$market = 'us'; // string | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
$offset = 0; // int | Zero-based result offset for pagination
$safe_search = 'safe_search_example'; // string | off | moderate | strict (default moderate)

try {
    $result = $apiInstance->yahooWebSearch($query, $market, $offset, $safe_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YahooApi->yahooWebSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;coffee machine&#39; | |
| **market** | **string**| Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &#39;us&#39;] |
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

## `yahooYahooScraperHealthCheck()`

```php
yahooYahooScraperHealthCheck(): mixed
```

Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YahooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->yahooYahooScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YahooApi->yahooYahooScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `yahooYahooScraperHealthCheckHead()`

```php
yahooYahooScraperHealthCheckHead(): mixed
```

Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YahooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->yahooYahooScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YahooApi->yahooYahooScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

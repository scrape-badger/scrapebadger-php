# ScrapeBadger\DuckDuckGoApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**duckduckgoDuckduckgoScraperHealthCheck()**](DuckDuckGoApi.md#duckduckgoDuckduckgoScraperHealthCheck) | **GET** /v1/duckduckgo/health | DuckDuckGo scraper health check |
| [**duckduckgoDuckduckgoScraperHealthCheckHead()**](DuckDuckGoApi.md#duckduckgoDuckduckgoScraperHealthCheckHead) | **HEAD** /v1/duckduckgo/health | DuckDuckGo scraper health check |
| [**duckduckgoImageSearch()**](DuckDuckGoApi.md#duckduckgoImageSearch) | **GET** /v1/duckduckgo/images | Image search |
| [**duckduckgoInstantAnswer()**](DuckDuckGoApi.md#duckduckgoInstantAnswer) | **GET** /v1/duckduckgo/instant | Instant Answer |
| [**duckduckgoListSupportedRegions()**](DuckDuckGoApi.md#duckduckgoListSupportedRegions) | **GET** /v1/duckduckgo/regions | List supported regions |
| [**duckduckgoNewsSearch()**](DuckDuckGoApi.md#duckduckgoNewsSearch) | **GET** /v1/duckduckgo/news | News search |
| [**duckduckgoSearchSuggestions()**](DuckDuckGoApi.md#duckduckgoSearchSuggestions) | **GET** /v1/duckduckgo/autocomplete | Search suggestions |
| [**duckduckgoVideoSearch()**](DuckDuckGoApi.md#duckduckgoVideoSearch) | **GET** /v1/duckduckgo/videos | Video search |
| [**duckduckgoWebSearch()**](DuckDuckGoApi.md#duckduckgoWebSearch) | **GET** /v1/duckduckgo/search | Web search |


## `duckduckgoDuckduckgoScraperHealthCheck()`

```php
duckduckgoDuckduckgoScraperHealthCheck(): mixed
```

DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DuckDuckGoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->duckduckgoDuckduckgoScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DuckDuckGoApi->duckduckgoDuckduckgoScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `duckduckgoDuckduckgoScraperHealthCheckHead()`

```php
duckduckgoDuckduckgoScraperHealthCheckHead(): mixed
```

DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DuckDuckGoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->duckduckgoDuckduckgoScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DuckDuckGoApi->duckduckgoDuckduckgoScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `duckduckgoImageSearch()`

```php
duckduckgoImageSearch($query, $region, $safesearch, $page, $size, $color, $image_type, $layout, $license): mixed
```

Image search

DuckDuckGo image search with size/color/type/layout/license filters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DuckDuckGoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search query
$region = 'wt-wt'; // string | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
$safesearch = 'moderate'; // string | on | moderate | off
$page = 1; // int | 100 results per page
$size = ''; // string | Small | Medium | Large | Wallpaper
$color = ''; // string | color | Monochrome | Red | Blue | …
$image_type = ''; // string | photo | clipart | gif | transparent | line
$layout = ''; // string | Square | Tall | Wide
$license = ''; // string | Any | Public | Share | ShareCommercially | Modify

try {
    $result = $apiInstance->duckduckgoImageSearch($query, $region, $safesearch, $page, $size, $color, $image_type, $layout, $license);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DuckDuckGoApi->duckduckgoImageSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search query | |
| **region** | **string**| DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &#39;wt-wt&#39;] |
| **safesearch** | **string**| on | moderate | off | [optional] [default to &#39;moderate&#39;] |
| **page** | **int**| 100 results per page | [optional] [default to 1] |
| **size** | **string**| Small | Medium | Large | Wallpaper | [optional] [default to &#39;&#39;] |
| **color** | **string**| color | Monochrome | Red | Blue | … | [optional] [default to &#39;&#39;] |
| **image_type** | **string**| photo | clipart | gif | transparent | line | [optional] [default to &#39;&#39;] |
| **layout** | **string**| Square | Tall | Wide | [optional] [default to &#39;&#39;] |
| **license** | **string**| Any | Public | Share | ShareCommercially | Modify | [optional] [default to &#39;&#39;] |

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

## `duckduckgoInstantAnswer()`

```php
duckduckgoInstantAnswer($query): mixed
```

Instant Answer

DuckDuckGo Instant Answer — abstract, definition, direct answer, related topics.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DuckDuckGoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Query for the Instant Answer API

try {
    $result = $apiInstance->duckduckgoInstantAnswer($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DuckDuckGoApi->duckduckgoInstantAnswer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Query for the Instant Answer API | |

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

## `duckduckgoListSupportedRegions()`

```php
duckduckgoListSupportedRegions(): mixed
```

List supported regions

The full DuckDuckGo region (kl) code list.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DuckDuckGoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->duckduckgoListSupportedRegions();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DuckDuckGoApi->duckduckgoListSupportedRegions: ', $e->getMessage(), PHP_EOL;
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

## `duckduckgoNewsSearch()`

```php
duckduckgoNewsSearch($query, $region, $safesearch, $timelimit, $page): mixed
```

News search

DuckDuckGo news search — headline, source, excerpt, unix + ISO date, image.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DuckDuckGoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search query
$region = 'wt-wt'; // string | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
$safesearch = 'moderate'; // string | on | moderate | off
$timelimit = ''; // string | day | week | month | year
$page = 1; // int | 30 results per page

try {
    $result = $apiInstance->duckduckgoNewsSearch($query, $region, $safesearch, $timelimit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DuckDuckGoApi->duckduckgoNewsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search query | |
| **region** | **string**| DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &#39;wt-wt&#39;] |
| **safesearch** | **string**| on | moderate | off | [optional] [default to &#39;moderate&#39;] |
| **timelimit** | **string**| day | week | month | year | [optional] [default to &#39;&#39;] |
| **page** | **int**| 30 results per page | [optional] [default to 1] |

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

## `duckduckgoSearchSuggestions()`

```php
duckduckgoSearchSuggestions($query, $region): mixed
```

Search suggestions

DuckDuckGo search-box suggestions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DuckDuckGoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial query to complete
$region = 'wt-wt'; // string | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.

try {
    $result = $apiInstance->duckduckgoSearchSuggestions($query, $region);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DuckDuckGoApi->duckduckgoSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial query to complete | |
| **region** | **string**| DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &#39;wt-wt&#39;] |

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

## `duckduckgoVideoSearch()`

```php
duckduckgoVideoSearch($query, $region, $safesearch, $page, $duration, $resolution): mixed
```

Video search

DuckDuckGo video search — title, publisher, uploader, duration, views, thumbnails.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DuckDuckGoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search query
$region = 'wt-wt'; // string | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
$safesearch = 'moderate'; // string | on | moderate | off
$page = 1; // int | 60 results per page
$duration = ''; // string | short | medium | long
$resolution = ''; // string | high | standard

try {
    $result = $apiInstance->duckduckgoVideoSearch($query, $region, $safesearch, $page, $duration, $resolution);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DuckDuckGoApi->duckduckgoVideoSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search query | |
| **region** | **string**| DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &#39;wt-wt&#39;] |
| **safesearch** | **string**| on | moderate | off | [optional] [default to &#39;moderate&#39;] |
| **page** | **int**| 60 results per page | [optional] [default to 1] |
| **duration** | **string**| short | medium | long | [optional] [default to &#39;&#39;] |
| **resolution** | **string**| high | standard | [optional] [default to &#39;&#39;] |

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

## `duckduckgoWebSearch()`

```php
duckduckgoWebSearch($query, $region, $safesearch, $timelimit, $page): mixed
```

Web search

DuckDuckGo web SERP — organic results, the zero-click abstract box, ads flagged.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DuckDuckGoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search query
$region = 'wt-wt'; // string | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
$safesearch = 'moderate'; // string | on | moderate | off
$timelimit = ''; // string | day | week | month | year
$page = 1; // int

try {
    $result = $apiInstance->duckduckgoWebSearch($query, $region, $safesearch, $timelimit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DuckDuckGoApi->duckduckgoWebSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search query | |
| **region** | **string**| DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &#39;wt-wt&#39;] |
| **safesearch** | **string**| on | moderate | off | [optional] [default to &#39;moderate&#39;] |
| **timelimit** | **string**| day | week | month | year | [optional] [default to &#39;&#39;] |
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

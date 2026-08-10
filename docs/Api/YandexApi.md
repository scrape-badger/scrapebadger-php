# ScrapeBadger\YandexApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**yandexImageSearch()**](YandexApi.md#yandexImageSearch) | **GET** /v1/yandex/images/search | Image search |
| [**yandexListSupportedMarkets()**](YandexApi.md#yandexListSupportedMarkets) | **GET** /v1/yandex/markets | List supported markets |
| [**yandexReverseImageSearch()**](YandexApi.md#yandexReverseImageSearch) | **GET** /v1/yandex/images/reverse | Reverse image search |
| [**yandexWebSearch()**](YandexApi.md#yandexWebSearch) | **GET** /v1/yandex/search | Web search |
| [**yandexYandexScraperHealthCheck()**](YandexApi.md#yandexYandexScraperHealthCheck) | **GET** /v1/yandex/health | Yandex scraper health check |
| [**yandexYandexScraperHealthCheckHead()**](YandexApi.md#yandexYandexScraperHealthCheckHead) | **HEAD** /v1/yandex/health | Yandex scraper health check |


## `yandexImageSearch()`

```php
yandexImageSearch($query, $domain, $page): mixed
```

Image search

Search Yandex Images by text — thumbnail, full-res URL, dimensions, source page.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YandexApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Image search query, e.g. 'coffee machine'
$domain = 'tr'; // string | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate.
$page = 1; // int

try {
    $result = $apiInstance->yandexImageSearch($query, $domain, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YandexApi->yandexImageSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Image search query, e.g. &#39;coffee machine&#39; | |
| **domain** | **string**| Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to &#39;tr&#39;] |
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

## `yandexListSupportedMarkets()`

```php
yandexListSupportedMarkets(): mixed
```

List supported markets

Supported Yandex markets (domains, default region and language).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YandexApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->yandexListSupportedMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YandexApi->yandexListSupportedMarkets: ', $e->getMessage(), PHP_EOL;
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

## `yandexReverseImageSearch()`

```php
yandexReverseImageSearch($image_url, $domain): mixed
```

Reverse image search

Reverse image search by URL — hosting pages, similar images, tags, other sizes.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YandexApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$image_url = 'image_url_example'; // string | Public URL of the image to reverse-search
$domain = 'tr'; // string | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate.

try {
    $result = $apiInstance->yandexReverseImageSearch($image_url, $domain);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YandexApi->yandexReverseImageSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **image_url** | **string**| Public URL of the image to reverse-search | |
| **domain** | **string**| Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to &#39;tr&#39;] |

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

## `yandexWebSearch()`

```php
yandexWebSearch($query, $domain, $page, $lr, $lang): mixed
```

Web search

Search Yandex web results — organic results, ads, displayed URLs, snippets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YandexApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search query, e.g. 'coffee machine'
$domain = 'tr'; // string | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate.
$page = 1; // int
$lr = 56; // int | Yandex region id, e.g. 213=Moscow, 84=USA
$lang = 'lang_example'; // string | UI language: ru, en, tr, be, kk, uk

try {
    $result = $apiInstance->yandexWebSearch($query, $domain, $page, $lr, $lang);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YandexApi->yandexWebSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search query, e.g. &#39;coffee machine&#39; | |
| **domain** | **string**| Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to &#39;tr&#39;] |
| **page** | **int**|  | [optional] [default to 1] |
| **lr** | **int**| Yandex region id, e.g. 213&#x3D;Moscow, 84&#x3D;USA | [optional] |
| **lang** | **string**| UI language: ru, en, tr, be, kk, uk | [optional] |

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

## `yandexYandexScraperHealthCheck()`

```php
yandexYandexScraperHealthCheck(): mixed
```

Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YandexApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->yandexYandexScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YandexApi->yandexYandexScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `yandexYandexScraperHealthCheckHead()`

```php
yandexYandexScraperHealthCheckHead(): mixed
```

Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YandexApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->yandexYandexScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YandexApi->yandexYandexScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

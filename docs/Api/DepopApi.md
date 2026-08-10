# ScrapeBadger\DepopApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**depopDepopScraperHealthCheck()**](DepopApi.md#depopDepopScraperHealthCheck) | **GET** /v1/depop/health | Depop scraper health check |
| [**depopDepopScraperHealthCheckHead()**](DepopApi.md#depopDepopScraperHealthCheckHead) | **HEAD** /v1/depop/health | Depop scraper health check |
| [**depopGetAUserSProducts()**](DepopApi.md#depopGetAUserSProducts) | **GET** /v1/depop/users/{username}/products | Get a user&#39;s products |
| [**depopGetProductDetail()**](DepopApi.md#depopGetProductDetail) | **GET** /v1/depop/products/{product_id} | Get product detail |
| [**depopGetShopUserProfile()**](DepopApi.md#depopGetShopUserProfile) | **GET** /v1/depop/users/{username} | Get shop/user profile |
| [**depopListMarkets()**](DepopApi.md#depopListMarkets) | **GET** /v1/depop/markets | List markets |
| [**depopSearchDepopProducts()**](DepopApi.md#depopSearchDepopProducts) | **GET** /v1/depop/search | Search Depop products |


## `depopDepopScraperHealthCheck()`

```php
depopDepopScraperHealthCheck(): mixed
```

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DepopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->depopDepopScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DepopApi->depopDepopScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `depopDepopScraperHealthCheckHead()`

```php
depopDepopScraperHealthCheckHead(): mixed
```

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DepopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->depopDepopScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DepopApi->depopDepopScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `depopGetAUserSProducts()`

```php
depopGetAUserSProducts($username, $market, $per_page, $cursor): mixed
```

Get a user's products

A user's active listings (cursor-paginated).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DepopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$market = 'us'; // string | Market code
$per_page = 24; // int
$cursor = 'cursor_example'; // string | Pagination cursor

try {
    $result = $apiInstance->depopGetAUserSProducts($username, $market, $per_page, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DepopApi->depopGetAUserSProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **market** | **string**| Market code | [optional] [default to &#39;us&#39;] |
| **per_page** | **int**|  | [optional] [default to 24] |
| **cursor** | **string**| Pagination cursor | [optional] |

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

## `depopGetProductDetail()`

```php
depopGetProductDetail($product_id, $market): mixed
```

Get product detail

Full detail for a single product (by numeric id or slug).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DepopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 'product_id_example'; // string
$market = 'us'; // string | Market code

try {
    $result = $apiInstance->depopGetProductDetail($product_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DepopApi->depopGetProductDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **string**|  | |
| **market** | **string**| Market code | [optional] [default to &#39;us&#39;] |

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

## `depopGetShopUserProfile()`

```php
depopGetShopUserProfile($username, $market): mixed
```

Get shop/user profile

Public shop/user profile by username.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DepopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$market = 'us'; // string | Market code

try {
    $result = $apiInstance->depopGetShopUserProfile($username, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DepopApi->depopGetShopUserProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **market** | **string**| Market code | [optional] [default to &#39;us&#39;] |

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

## `depopListMarkets()`

```php
depopListMarkets(): mixed
```

List markets

List supported Depop markets (country + currency).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DepopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->depopListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DepopApi->depopListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `depopSearchDepopProducts()`

```php
depopSearchDepopProducts($query, $market, $per_page, $cursor, $price_min, $price_max, $brands, $categories, $sizes, $conditions, $gender, $sort): mixed
```

Search Depop products

Search the Depop catalog with filters (cursor-paginated).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\DepopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search text, e.g. 'nike vintage'
$market = 'us'; // string | Market code (us, gb, au, it, fr, ...)
$per_page = 24; // int | Results per page
$cursor = 'cursor_example'; // string | Pagination cursor (from previous page)
$price_min = 3.4; // float | Minimum price
$price_max = 3.4; // float | Maximum price
$brands = 'brands_example'; // string | Comma-separated brand IDs
$categories = 'categories_example'; // string | Comma-separated category IDs
$sizes = 'sizes_example'; // string | Comma-separated size IDs
$conditions = 'conditions_example'; // string | Comma-separated condition slugs (brand_new, used_excellent, ...)
$gender = 'gender_example'; // string | male | female
$sort = 'sort_example'; // string | relevance | newlyListed | priceAscending | priceDescending

try {
    $result = $apiInstance->depopSearchDepopProducts($query, $market, $per_page, $cursor, $price_min, $price_max, $brands, $categories, $sizes, $conditions, $gender, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DepopApi->depopSearchDepopProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search text, e.g. &#39;nike vintage&#39; | |
| **market** | **string**| Market code (us, gb, au, it, fr, ...) | [optional] [default to &#39;us&#39;] |
| **per_page** | **int**| Results per page | [optional] [default to 24] |
| **cursor** | **string**| Pagination cursor (from previous page) | [optional] |
| **price_min** | **float**| Minimum price | [optional] |
| **price_max** | **float**| Maximum price | [optional] |
| **brands** | **string**| Comma-separated brand IDs | [optional] |
| **categories** | **string**| Comma-separated category IDs | [optional] |
| **sizes** | **string**| Comma-separated size IDs | [optional] |
| **conditions** | **string**| Comma-separated condition slugs (brand_new, used_excellent, ...) | [optional] |
| **gender** | **string**| male | female | [optional] |
| **sort** | **string**| relevance | newlyListed | priceAscending | priceDescending | [optional] |

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

# ScrapeBadger\BestBuyApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bestbuyBrowseACategory()**](BestBuyApi.md#bestbuyBrowseACategory) | **GET** /v1/bestbuy/category | Browse a category |
| [**bestbuyGetCategories()**](BestBuyApi.md#bestbuyGetCategories) | **GET** /v1/bestbuy/categories | Get categories |
| [**bestbuyGetLaptopAndComputerDeals()**](BestBuyApi.md#bestbuyGetLaptopAndComputerDeals) | **GET** /v1/bestbuy/deals | Get laptop and computer deals |
| [**bestbuyGetProductAvailability()**](BestBuyApi.md#bestbuyGetProductAvailability) | **GET** /v1/bestbuy/products/{sku}/availability | Get product availability |
| [**bestbuyGetProductDetail()**](BestBuyApi.md#bestbuyGetProductDetail) | **GET** /v1/bestbuy/products/{sku} | Get product detail |
| [**bestbuyGetProductQuestions()**](BestBuyApi.md#bestbuyGetProductQuestions) | **GET** /v1/bestbuy/products/{sku}/questions | Get product questions |
| [**bestbuyGetProductReviews()**](BestBuyApi.md#bestbuyGetProductReviews) | **GET** /v1/bestbuy/products/{sku}/reviews | Get product reviews |
| [**bestbuyGetSearchSuggestions()**](BestBuyApi.md#bestbuyGetSearchSuggestions) | **GET** /v1/bestbuy/autocomplete | Get search suggestions |
| [**bestbuyListSupportedMarkets()**](BestBuyApi.md#bestbuyListSupportedMarkets) | **GET** /v1/bestbuy/markets | List supported markets |
| [**bestbuySearchProducts()**](BestBuyApi.md#bestbuySearchProducts) | **GET** /v1/bestbuy/search | Search products |


## `bestbuyBrowseACategory()`

```php
bestbuyBrowseACategory($category_id, $page): mixed
```

Browse a category

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BestBuyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = 'category_id_example'; // string
$page = 1; // int

try {
    $result = $apiInstance->bestbuyBrowseACategory($category_id, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BestBuyApi->bestbuyBrowseACategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **string**|  | |
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

## `bestbuyGetCategories()`

```php
bestbuyGetCategories($query): mixed
```

Get categories

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BestBuyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'laptop'; // string

try {
    $result = $apiInstance->bestbuyGetCategories($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BestBuyApi->bestbuyGetCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | [optional] [default to &#39;laptop&#39;] |

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

## `bestbuyGetLaptopAndComputerDeals()`

```php
bestbuyGetLaptopAndComputerDeals($page): mixed
```

Get laptop and computer deals

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BestBuyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int

try {
    $result = $apiInstance->bestbuyGetLaptopAndComputerDeals($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BestBuyApi->bestbuyGetLaptopAndComputerDeals: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `bestbuyGetProductAvailability()`

```php
bestbuyGetProductAvailability($sku, $zip_code, $store_id): mixed
```

Get product availability

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BestBuyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sku = 'sku_example'; // string
$zip_code = 'zip_code_example'; // string
$store_id = '7'; // string

try {
    $result = $apiInstance->bestbuyGetProductAvailability($sku, $zip_code, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BestBuyApi->bestbuyGetProductAvailability: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sku** | **string**|  | |
| **zip_code** | **string**|  | |
| **store_id** | **string**|  | [optional] [default to &#39;7&#39;] |

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

## `bestbuyGetProductDetail()`

```php
bestbuyGetProductDetail($sku): mixed
```

Get product detail

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BestBuyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sku = 'sku_example'; // string

try {
    $result = $apiInstance->bestbuyGetProductDetail($sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BestBuyApi->bestbuyGetProductDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sku** | **string**|  | |

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

## `bestbuyGetProductQuestions()`

```php
bestbuyGetProductQuestions($sku, $page, $page_size, $query): mixed
```

Get product questions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BestBuyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sku = 'sku_example'; // string
$page = 1; // int
$page_size = 10; // int
$query = ''; // string

try {
    $result = $apiInstance->bestbuyGetProductQuestions($sku, $page, $page_size, $query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BestBuyApi->bestbuyGetProductQuestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sku** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 10] |
| **query** | **string**|  | [optional] [default to &#39;&#39;] |

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

## `bestbuyGetProductReviews()`

```php
bestbuyGetProductReviews($sku, $page, $page_size, $sort): mixed
```

Get product reviews

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BestBuyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sku = 'sku_example'; // string
$page = 1; // int
$page_size = 10; // int
$sort = 'MOST_RECENT'; // string

try {
    $result = $apiInstance->bestbuyGetProductReviews($sku, $page, $page_size, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BestBuyApi->bestbuyGetProductReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sku** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 10] |
| **sort** | **string**|  | [optional] [default to &#39;MOST_RECENT&#39;] |

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

## `bestbuyGetSearchSuggestions()`

```php
bestbuyGetSearchSuggestions($query): mixed
```

Get search suggestions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BestBuyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string

try {
    $result = $apiInstance->bestbuyGetSearchSuggestions($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BestBuyApi->bestbuyGetSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |

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

## `bestbuyListSupportedMarkets()`

```php
bestbuyListSupportedMarkets(): mixed
```

List supported markets

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BestBuyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->bestbuyListSupportedMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BestBuyApi->bestbuyListSupportedMarkets: ', $e->getMessage(), PHP_EOL;
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

## `bestbuySearchProducts()`

```php
bestbuySearchProducts($query, $page, $sort): mixed
```

Search products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BestBuyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$page = 1; // int
$sort = 'best_match'; // string

try {
    $result = $apiInstance->bestbuySearchProducts($query, $page, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BestBuyApi->bestbuySearchProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **sort** | **string**|  | [optional] [default to &#39;best_match&#39;] |

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

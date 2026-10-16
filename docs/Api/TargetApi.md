# ScrapeBadger\TargetApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**targetBrowseACategory()**](TargetApi.md#targetBrowseACategory) | **GET** /v1/target/category | Browse a category |
| [**targetFindNearbyStores()**](TargetApi.md#targetFindNearbyStores) | **GET** /v1/target/stores | Find nearby stores |
| [**targetGetCategories()**](TargetApi.md#targetGetCategories) | **GET** /v1/target/categories | Get categories |
| [**targetGetProductAvailability()**](TargetApi.md#targetGetProductAvailability) | **GET** /v1/target/products/{tcin}/availability | Get product availability |
| [**targetGetProductDetail()**](TargetApi.md#targetGetProductDetail) | **GET** /v1/target/products/{tcin} | Get product detail |
| [**targetGetProductQuestions()**](TargetApi.md#targetGetProductQuestions) | **GET** /v1/target/products/{tcin}/questions | Get product questions |
| [**targetGetProductReviews()**](TargetApi.md#targetGetProductReviews) | **GET** /v1/target/products/{tcin}/reviews | Get product reviews |
| [**targetGetSearchSuggestions()**](TargetApi.md#targetGetSearchSuggestions) | **GET** /v1/target/autocomplete | Get search suggestions |
| [**targetGetStoreDetail()**](TargetApi.md#targetGetStoreDetail) | **GET** /v1/target/stores/{store_id} | Get store detail |
| [**targetListSupportedMarkets()**](TargetApi.md#targetListSupportedMarkets) | **GET** /v1/target/markets | List supported markets |
| [**targetSearchProducts()**](TargetApi.md#targetSearchProducts) | **GET** /v1/target/search | Search products |


## `targetBrowseACategory()`

```php
targetBrowseACategory($category_id, $page, $page_size, $store_id, $zip_code): mixed
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


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = 'category_id_example'; // string
$page = 1; // int
$page_size = 24; // int
$store_id = '1375'; // string
$zip_code = '55403'; // string

try {
    $result = $apiInstance->targetBrowseACategory($category_id, $page, $page_size, $store_id, $zip_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetBrowseACategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 24] |
| **store_id** | **string**|  | [optional] [default to &#39;1375&#39;] |
| **zip_code** | **string**|  | [optional] [default to &#39;55403&#39;] |

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

## `targetFindNearbyStores()`

```php
targetFindNearbyStores($zip_code, $limit): mixed
```

Find nearby stores

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$zip_code = 'zip_code_example'; // string
$limit = 10; // int

try {
    $result = $apiInstance->targetFindNearbyStores($zip_code, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetFindNearbyStores: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **zip_code** | **string**|  | |
| **limit** | **int**|  | [optional] [default to 10] |

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

## `targetGetCategories()`

```php
targetGetCategories($category_id): mixed
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


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = '5xtly'; // string

try {
    $result = $apiInstance->targetGetCategories($category_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetGetCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **string**|  | [optional] [default to &#39;5xtly&#39;] |

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

## `targetGetProductAvailability()`

```php
targetGetProductAvailability($tcin, $zip_code, $limit): mixed
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


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tcin = 'tcin_example'; // string
$zip_code = 'zip_code_example'; // string
$limit = 10; // int

try {
    $result = $apiInstance->targetGetProductAvailability($tcin, $zip_code, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetGetProductAvailability: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tcin** | **string**|  | |
| **zip_code** | **string**|  | |
| **limit** | **int**|  | [optional] [default to 10] |

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

## `targetGetProductDetail()`

```php
targetGetProductDetail($tcin, $store_id, $zip_code): mixed
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


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tcin = 'tcin_example'; // string
$store_id = '1375'; // string
$zip_code = '55403'; // string

try {
    $result = $apiInstance->targetGetProductDetail($tcin, $store_id, $zip_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetGetProductDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tcin** | **string**|  | |
| **store_id** | **string**|  | [optional] [default to &#39;1375&#39;] |
| **zip_code** | **string**|  | [optional] [default to &#39;55403&#39;] |

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

## `targetGetProductQuestions()`

```php
targetGetProductQuestions($tcin, $page, $page_size): mixed
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


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tcin = 'tcin_example'; // string
$page = 1; // int
$page_size = 10; // int

try {
    $result = $apiInstance->targetGetProductQuestions($tcin, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetGetProductQuestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tcin** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 10] |

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

## `targetGetProductReviews()`

```php
targetGetProductReviews($tcin, $page, $page_size, $sort): mixed
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


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tcin = 'tcin_example'; // string
$page = 1; // int
$page_size = 10; // int
$sort = 'most_recent'; // string

try {
    $result = $apiInstance->targetGetProductReviews($tcin, $page, $page_size, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetGetProductReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tcin** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 10] |
| **sort** | **string**|  | [optional] [default to &#39;most_recent&#39;] |

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

## `targetGetSearchSuggestions()`

```php
targetGetSearchSuggestions($query): mixed
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


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string

try {
    $result = $apiInstance->targetGetSearchSuggestions($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetGetSearchSuggestions: ', $e->getMessage(), PHP_EOL;
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

## `targetGetStoreDetail()`

```php
targetGetStoreDetail($store_id): mixed
```

Get store detail

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string

try {
    $result = $apiInstance->targetGetStoreDetail($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetGetStoreDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**|  | |

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

## `targetListSupportedMarkets()`

```php
targetListSupportedMarkets(): mixed
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


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->targetListSupportedMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetListSupportedMarkets: ', $e->getMessage(), PHP_EOL;
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

## `targetSearchProducts()`

```php
targetSearchProducts($query, $page, $page_size, $store_id, $zip_code, $sort): mixed
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


$apiInstance = new ScrapeBadger\Api\TargetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$page = 1; // int
$page_size = 24; // int
$store_id = '1375'; // string
$zip_code = '55403'; // string
$sort = 'relevance'; // string

try {
    $result = $apiInstance->targetSearchProducts($query, $page, $page_size, $store_id, $zip_code, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TargetApi->targetSearchProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 24] |
| **store_id** | **string**|  | [optional] [default to &#39;1375&#39;] |
| **zip_code** | **string**|  | [optional] [default to &#39;55403&#39;] |
| **sort** | **string**|  | [optional] [default to &#39;relevance&#39;] |

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

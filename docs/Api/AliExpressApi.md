# ScrapeBadger\AliExpressApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aliexpressGetCategoryNavigation()**](AliExpressApi.md#aliexpressGetCategoryNavigation) | **GET** /v1/aliexpress/categories | Get category navigation |
| [**aliexpressGetProductDetail()**](AliExpressApi.md#aliexpressGetProductDetail) | **GET** /v1/aliexpress/products/{product_id} | Get product detail |
| [**aliexpressGetProductReviews()**](AliExpressApi.md#aliexpressGetProductReviews) | **GET** /v1/aliexpress/products/{product_id}/reviews | Get product reviews |
| [**aliexpressGetSearchSuggestions()**](AliExpressApi.md#aliexpressGetSearchSuggestions) | **GET** /v1/aliexpress/autocomplete | Get search suggestions |
| [**aliexpressGetStoreProductCategories()**](AliExpressApi.md#aliexpressGetStoreProductCategories) | **GET** /v1/aliexpress/stores/{store_id}/categories | Get store product categories |
| [**aliexpressGetStoreProducts()**](AliExpressApi.md#aliexpressGetStoreProducts) | **GET** /v1/aliexpress/stores/{store_id}/products | Get store products |
| [**aliexpressGetStoreProfile()**](AliExpressApi.md#aliexpressGetStoreProfile) | **GET** /v1/aliexpress/stores/{store_id} | Get store profile |
| [**aliexpressSearchProducts()**](AliExpressApi.md#aliexpressSearchProducts) | **GET** /v1/aliexpress/search | Search products |


## `aliexpressGetCategoryNavigation()`

```php
aliexpressGetCategoryNavigation(): mixed
```

Get category navigation

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AliExpressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->aliexpressGetCategoryNavigation();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AliExpressApi->aliexpressGetCategoryNavigation: ', $e->getMessage(), PHP_EOL;
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

## `aliexpressGetProductDetail()`

```php
aliexpressGetProductDetail($product_id, $country, $currency, $language): mixed
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


$apiInstance = new ScrapeBadger\Api\AliExpressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 'product_id_example'; // string
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en_US'; // string

try {
    $result = $apiInstance->aliexpressGetProductDetail($product_id, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AliExpressApi->aliexpressGetProductDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **string**|  | |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en_US&#39;] |

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

## `aliexpressGetProductReviews()`

```php
aliexpressGetProductReviews($product_id, $page, $page_size, $sort): mixed
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


$apiInstance = new ScrapeBadger\Api\AliExpressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 'product_id_example'; // string
$page = 1; // int
$page_size = 10; // int
$sort = 'complex_default'; // string

try {
    $result = $apiInstance->aliexpressGetProductReviews($product_id, $page, $page_size, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AliExpressApi->aliexpressGetProductReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 10] |
| **sort** | **string**|  | [optional] [default to &#39;complex_default&#39;] |

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

## `aliexpressGetSearchSuggestions()`

```php
aliexpressGetSearchSuggestions($query, $country, $language): mixed
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


$apiInstance = new ScrapeBadger\Api\AliExpressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$country = 'US'; // string
$language = 'en'; // string

try {
    $result = $apiInstance->aliexpressGetSearchSuggestions($query, $country, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AliExpressApi->aliexpressGetSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en&#39;] |

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

## `aliexpressGetStoreProductCategories()`

```php
aliexpressGetStoreProductCategories($store_id, $country): mixed
```

Get store product categories

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AliExpressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string
$country = 'US'; // string

try {
    $result = $apiInstance->aliexpressGetStoreProductCategories($store_id, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AliExpressApi->aliexpressGetStoreProductCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**|  | |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |

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

## `aliexpressGetStoreProducts()`

```php
aliexpressGetStoreProducts($store_id, $page, $page_size, $country, $currency, $language, $query, $sort): mixed
```

Get store products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AliExpressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string
$page = 1; // int
$page_size = 24; // int
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en'; // string
$query = ''; // string
$sort = 'bestmatch_sort'; // string

try {
    $result = $apiInstance->aliexpressGetStoreProducts($store_id, $page, $page_size, $country, $currency, $language, $query, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AliExpressApi->aliexpressGetStoreProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 24] |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en&#39;] |
| **query** | **string**|  | [optional] [default to &#39;&#39;] |
| **sort** | **string**|  | [optional] [default to &#39;bestmatch_sort&#39;] |

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

## `aliexpressGetStoreProfile()`

```php
aliexpressGetStoreProfile($store_id, $country, $currency, $language): mixed
```

Get store profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AliExpressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en'; // string

try {
    $result = $apiInstance->aliexpressGetStoreProfile($store_id, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AliExpressApi->aliexpressGetStoreProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**|  | |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en&#39;] |

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

## `aliexpressSearchProducts()`

```php
aliexpressSearchProducts($query, $page, $country, $currency, $language, $sort, $min_price, $max_price): mixed
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


$apiInstance = new ScrapeBadger\Api\AliExpressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$page = 1; // int
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en'; // string
$sort = 'default'; // string
$min_price = 3.4; // float
$max_price = 3.4; // float

try {
    $result = $apiInstance->aliexpressSearchProducts($query, $page, $country, $currency, $language, $sort, $min_price, $max_price);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AliExpressApi->aliexpressSearchProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en&#39;] |
| **sort** | **string**|  | [optional] [default to &#39;default&#39;] |
| **min_price** | **float**|  | [optional] |
| **max_price** | **float**|  | [optional] |

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

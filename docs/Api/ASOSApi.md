# ScrapeBadger\ASOSApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**asosGetProductDetail()**](ASOSApi.md#asosGetProductDetail) | **GET** /v1/asos/products/{product_id} | Get product detail |
| [**asosGetStockAndPrices()**](ASOSApi.md#asosGetStockAndPrices) | **GET** /v1/asos/stock-price | Get stock and prices |
| [**asosListCategories()**](ASOSApi.md#asosListCategories) | **GET** /v1/asos/categories | List categories |
| [**asosListMarkets()**](ASOSApi.md#asosListMarkets) | **GET** /v1/asos/markets | List markets |
| [**asosListSearchFilters()**](ASOSApi.md#asosListSearchFilters) | **GET** /v1/asos/filters | List search filters |
| [**asosSearchProducts()**](ASOSApi.md#asosSearchProducts) | **GET** /v1/asos/search | Search products |
| [**asosSearchSuggestions()**](ASOSApi.md#asosSearchSuggestions) | **GET** /v1/asos/autocomplete | Search suggestions |


## `asosGetProductDetail()`

```php
asosGetProductDetail($product_id, $market, $store, $country, $currency, $language): \ScrapeBadger\Model\ProductResponse
```

Get product detail

Product, live per-size stock and price, images, descriptions, reviews and breadcrumbs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ASOSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 56; // int
$market = 'uk'; // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
$store = 'store_example'; // string | Override store, e.g. COM or US
$country = 'country_example'; // string | ISO country override
$currency = 'currency_example'; // string | Currency override
$language = 'language_example'; // string | Locale override, e.g. en-GB

try {
    $result = $apiInstance->asosGetProductDetail($product_id, $market, $store, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ASOSApi->asosGetProductDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **int**|  | |
| **market** | **string**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &#39;uk&#39;] |
| **store** | **string**| Override store, e.g. COM or US | [optional] |
| **country** | **string**| ISO country override | [optional] |
| **currency** | **string**| Currency override | [optional] |
| **language** | **string**| Locale override, e.g. en-GB | [optional] |

### Return type

[**\ScrapeBadger\Model\ProductResponse**](../Model/ProductResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `asosGetStockAndPrices()`

```php
asosGetStockAndPrices($product_ids, $market, $store, $country, $currency, $language): \ScrapeBadger\Model\StockResponse
```

Get stock and prices

Refresh product and variant stock/prices; reports missing product ids explicitly.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ASOSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_ids = 'product_ids_example'; // string | 1–50 comma-separated product ids
$market = 'uk'; // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
$store = 'store_example'; // string | Override store, e.g. COM or US
$country = 'country_example'; // string | ISO country override
$currency = 'currency_example'; // string | Currency override
$language = 'language_example'; // string | Locale override, e.g. en-GB

try {
    $result = $apiInstance->asosGetStockAndPrices($product_ids, $market, $store, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ASOSApi->asosGetStockAndPrices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_ids** | **string**| 1–50 comma-separated product ids | |
| **market** | **string**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &#39;uk&#39;] |
| **store** | **string**| Override store, e.g. COM or US | [optional] |
| **country** | **string**| ISO country override | [optional] |
| **currency** | **string**| Currency override | [optional] |
| **language** | **string**| Locale override, e.g. en-GB | [optional] |

### Return type

[**\ScrapeBadger\Model\StockResponse**](../Model/StockResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `asosListCategories()`

```php
asosListCategories($gender, $market, $store, $country, $currency, $language): mixed
```

List categories

Full nested navigation with category ids, names, images and links.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ASOSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$gender = 'men'; // string
$market = 'uk'; // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
$store = 'store_example'; // string | Override store, e.g. COM or US
$country = 'country_example'; // string | ISO country override
$currency = 'currency_example'; // string | Currency override
$language = 'language_example'; // string | Locale override, e.g. en-GB

try {
    $result = $apiInstance->asosListCategories($gender, $market, $store, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ASOSApi->asosListCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **gender** | **string**|  | [optional] [default to &#39;men&#39;] |
| **market** | **string**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &#39;uk&#39;] |
| **store** | **string**| Override store, e.g. COM or US | [optional] |
| **country** | **string**| ISO country override | [optional] |
| **currency** | **string**| Currency override | [optional] |
| **language** | **string**| Locale override, e.g. en-GB | [optional] |

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

## `asosListMarkets()`

```php
asosListMarkets(): mixed
```

List markets

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ASOSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->asosListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ASOSApi->asosListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `asosListSearchFilters()`

```php
asosListSearchFilters($query, $category_id, $market, $store, $country, $currency, $language): mixed
```

List search filters

Facet ids, labels, option counts and selections for a query or category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ASOSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$category_id = 56; // int
$market = 'uk'; // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
$store = 'store_example'; // string | Override store, e.g. COM or US
$country = 'country_example'; // string | ISO country override
$currency = 'currency_example'; // string | Currency override
$language = 'language_example'; // string | Locale override, e.g. en-GB

try {
    $result = $apiInstance->asosListSearchFilters($query, $category_id, $market, $store, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ASOSApi->asosListSearchFilters: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | [optional] |
| **category_id** | **int**|  | [optional] |
| **market** | **string**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &#39;uk&#39;] |
| **store** | **string**| Override store, e.g. COM or US | [optional] |
| **country** | **string**| ISO country override | [optional] |
| **currency** | **string**| Currency override | [optional] |
| **language** | **string**| Locale override, e.g. en-GB | [optional] |

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

## `asosSearchProducts()`

```php
asosSearchProducts($query, $category_id, $offset, $limit, $sort, $brand, $colour, $size, $min_price, $max_price, $market, $store, $country, $currency, $language): \ScrapeBadger\Model\PortalApiRoutersV1AsosSearchResponse
```

Search products

Search by query, category_id, or both. Includes price, images and filter facets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ASOSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Keyword, e.g. shoes
$category_id = 56; // int | Category id from navigation
$offset = 0; // int
$limit = 48; // int
$sort = 'recommended'; // string
$brand = 'brand_example'; // string | Comma-separated brand facet ids
$colour = 'colour_example'; // string | Comma-separated colour facet ids
$size = 'size_example'; // string | Comma-separated size facet ids
$min_price = 3.4; // float
$max_price = 3.4; // float
$market = 'uk'; // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
$store = 'store_example'; // string | Override store, e.g. COM or US
$country = 'country_example'; // string | ISO country override
$currency = 'currency_example'; // string | Currency override
$language = 'language_example'; // string | Locale override, e.g. en-GB

try {
    $result = $apiInstance->asosSearchProducts($query, $category_id, $offset, $limit, $sort, $brand, $colour, $size, $min_price, $max_price, $market, $store, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ASOSApi->asosSearchProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Keyword, e.g. shoes | [optional] |
| **category_id** | **int**| Category id from navigation | [optional] |
| **offset** | **int**|  | [optional] [default to 0] |
| **limit** | **int**|  | [optional] [default to 48] |
| **sort** | **string**|  | [optional] [default to &#39;recommended&#39;] |
| **brand** | **string**| Comma-separated brand facet ids | [optional] |
| **colour** | **string**| Comma-separated colour facet ids | [optional] |
| **size** | **string**| Comma-separated size facet ids | [optional] |
| **min_price** | **float**|  | [optional] |
| **max_price** | **float**|  | [optional] |
| **market** | **string**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &#39;uk&#39;] |
| **store** | **string**| Override store, e.g. COM or US | [optional] |
| **country** | **string**| ISO country override | [optional] |
| **currency** | **string**| Currency override | [optional] |
| **language** | **string**| Locale override, e.g. en-GB | [optional] |

### Return type

[**\ScrapeBadger\Model\PortalApiRoutersV1AsosSearchResponse**](../Model/PortalApiRoutersV1AsosSearchResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `asosSearchSuggestions()`

```php
asosSearchSuggestions($query, $market, $store, $country, $currency, $language): mixed
```

Search suggestions

Search suggestions with result counts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ASOSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$market = 'uk'; // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
$store = 'store_example'; // string | Override store, e.g. COM or US
$country = 'country_example'; // string | ISO country override
$currency = 'currency_example'; // string | Currency override
$language = 'language_example'; // string | Locale override, e.g. en-GB

try {
    $result = $apiInstance->asosSearchSuggestions($query, $market, $store, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ASOSApi->asosSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **market** | **string**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &#39;uk&#39;] |
| **store** | **string**| Override store, e.g. COM or US | [optional] |
| **country** | **string**| ISO country override | [optional] |
| **currency** | **string**| Currency override | [optional] |
| **language** | **string**| Locale override, e.g. en-GB | [optional] |

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

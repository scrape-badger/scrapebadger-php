# ScrapeBadger\WalmartApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**walmartBrowseACategory()**](WalmartApi.md#walmartBrowseACategory) | **GET** /v1/walmart/category | Browse a category |
| [**walmartDealsRollbacksAndClearance()**](WalmartApi.md#walmartDealsRollbacksAndClearance) | **GET** /v1/walmart/deals | Deals, rollbacks and clearance |
| [**walmartGetASellerSCatalogue()**](WalmartApi.md#walmartGetASellerSCatalogue) | **GET** /v1/walmart/sellers/{seller_id}/products | Get a seller&#39;s catalogue |
| [**walmartGetProductDetail()**](WalmartApi.md#walmartGetProductDetail) | **GET** /v1/walmart/products/{item_id} | Get product detail |
| [**walmartGetProductReviews()**](WalmartApi.md#walmartGetProductReviews) | **GET** /v1/walmart/products/{item_id}/reviews | Get product reviews |
| [**walmartGetSellerProfile()**](WalmartApi.md#walmartGetSellerProfile) | **GET** /v1/walmart/sellers/{seller_id} | Get seller profile |
| [**walmartGetStoreNearbyStores()**](WalmartApi.md#walmartGetStoreNearbyStores) | **GET** /v1/walmart/stores/{store_id} | Get store + nearby stores |
| [**walmartListSupportedMarkets()**](WalmartApi.md#walmartListSupportedMarkets) | **GET** /v1/walmart/markets | List supported markets |
| [**walmartSearchProducts()**](WalmartApi.md#walmartSearchProducts) | **GET** /v1/walmart/search | Search products |
| [**walmartSearchSuggestions()**](WalmartApi.md#walmartSearchSuggestions) | **GET** /v1/walmart/autocomplete | Search suggestions |
| [**walmartWalmartScraperHealthCheck()**](WalmartApi.md#walmartWalmartScraperHealthCheck) | **GET** /v1/walmart/health | Walmart scraper health check |
| [**walmartWalmartScraperHealthCheckHead()**](WalmartApi.md#walmartWalmartScraperHealthCheckHead) | **HEAD** /v1/walmart/health | Walmart scraper health check |


## `walmartBrowseACategory()`

```php
walmartBrowseACategory($path, $page, $min_price, $max_price, $facet): mixed
```

Browse a category

Browse a Walmart category. Same result shape as search.  No `sort`: Walmart's browse pages ignore it. Sort on `/search` instead.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$path = 'path_example'; // string | Browse path, e.g. 'electronics/3944', or a '/cp/...' path
$page = 1; // int
$min_price = 3.4; // float
$max_price = 3.4; // float
$facet = 'facet_example'; // string

try {
    $result = $apiInstance->walmartBrowseACategory($path, $page, $min_price, $max_price, $facet);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartBrowseACategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **path** | **string**| Browse path, e.g. &#39;electronics/3944&#39;, or a &#39;/cp/...&#39; path | |
| **page** | **int**|  | [optional] [default to 1] |
| **min_price** | **float**|  | [optional] |
| **max_price** | **float**|  | [optional] |
| **facet** | **string**|  | [optional] |

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

## `walmartDealsRollbacksAndClearance()`

```php
walmartDealsRollbacksAndClearance($page, $min_price, $max_price): mixed
```

Deals, rollbacks and clearance

Walmart's current deals, rollbacks and clearance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int
$min_price = 3.4; // float
$max_price = 3.4; // float

try {
    $result = $apiInstance->walmartDealsRollbacksAndClearance($page, $min_price, $max_price);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartDealsRollbacksAndClearance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] [default to 1] |
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

## `walmartGetASellerSCatalogue()`

```php
walmartGetASellerSCatalogue($seller_id, $query, $page, $sort): mixed
```

Get a seller's catalogue

A marketplace seller's catalogue, scoped by a search term.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$seller_id = 'seller_id_example'; // string | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s).
$query = 'query_example'; // string | Required — Walmart returns nothing for a seller facet alone
$page = 1; // int
$sort = 'sort_example'; // string

try {
    $result = $apiInstance->walmartGetASellerSCatalogue($seller_id, $query, $page, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartGetASellerSCatalogue: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **seller_id** | **string**| Numeric catalog seller id, e.g. &#39;101040442&#39; — the &#x60;catalog_seller_id&#x60; on a product, NOT the 32-char hex &#x60;seller_id&#x60; (which 404s). | |
| **query** | **string**| Required — Walmart returns nothing for a seller facet alone | |
| **page** | **int**|  | [optional] [default to 1] |
| **sort** | **string**|  | [optional] |

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

## `walmartGetProductDetail()`

```php
walmartGetProductDetail($item_id): mixed
```

Get product detail

Full product detail — price, stock, specs, variants, seller, reviews sample.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = 'item_id_example'; // string | Walmart usItemId, e.g. '5689919121'

try {
    $result = $apiInstance->walmartGetProductDetail($item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartGetProductDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **item_id** | **string**| Walmart usItemId, e.g. &#39;5689919121&#39; | |

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

## `walmartGetProductReviews()`

```php
walmartGetProductReviews($item_id, $page, $sort): mixed
```

Get product reviews

Paginated reviews with the full star histogram. 10 per page.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = 'item_id_example'; // string | Walmart usItemId, e.g. '5689919121'
$page = 1; // int
$sort = 'sort_example'; // string | relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful

try {
    $result = $apiInstance->walmartGetProductReviews($item_id, $page, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartGetProductReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **item_id** | **string**| Walmart usItemId, e.g. &#39;5689919121&#39; | |
| **page** | **int**|  | [optional] [default to 1] |
| **sort** | **string**| relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful | [optional] |

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

## `walmartGetSellerProfile()`

```php
walmartGetSellerProfile($seller_id): mixed
```

Get seller profile

Marketplace seller profile — contact details, address, rating, policies.  No `page`: adding one makes Walmart's own SSR throw. Use `/sellers/{id}/products` for the catalogue.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$seller_id = 'seller_id_example'; // string | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s).

try {
    $result = $apiInstance->walmartGetSellerProfile($seller_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartGetSellerProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **seller_id** | **string**| Numeric catalog seller id, e.g. &#39;101040442&#39; — the &#x60;catalog_seller_id&#x60; on a product, NOT the 32-char hex &#x60;seller_id&#x60; (which 404s). | |

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

## `walmartGetStoreNearbyStores()`

```php
walmartGetStoreNearbyStores($store_id): mixed
```

Get store + nearby stores

Store detail with hours, per-department services, and nearby stores.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_id = 'store_id_example'; // string | Walmart store number, e.g. '100'

try {
    $result = $apiInstance->walmartGetStoreNearbyStores($store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartGetStoreNearbyStores: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_id** | **string**| Walmart store number, e.g. &#39;100&#39; | |

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

## `walmartListSupportedMarkets()`

```php
walmartListSupportedMarkets(): mixed
```

List supported markets

Supported Walmart markets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->walmartListSupportedMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartListSupportedMarkets: ', $e->getMessage(), PHP_EOL;
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

## `walmartSearchProducts()`

```php
walmartSearchProducts($query, $page, $sort, $min_price, $max_price, $facet): mixed
```

Search products

Search walmart.com. ~40-60 organic products per page; ad tiles are dropped.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'laptop'
$page = 1; // int | Results dry up after page 10
$sort = 'sort_example'; // string | best_match | best_seller | price_low | price_high | rating_high | new
$min_price = 3.4; // float
$max_price = 3.4; // float
$facet = 'facet_example'; // string | Facet filter, e.g. 'brand:HP'

try {
    $result = $apiInstance->walmartSearchProducts($query, $page, $sort, $min_price, $max_price, $facet);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartSearchProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;laptop&#39; | |
| **page** | **int**| Results dry up after page 10 | [optional] [default to 1] |
| **sort** | **string**| best_match | best_seller | price_low | price_high | rating_high | new | [optional] |
| **min_price** | **float**|  | [optional] |
| **max_price** | **float**|  | [optional] |
| **facet** | **string**| Facet filter, e.g. &#39;brand:HP&#39; | [optional] |

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

## `walmartSearchSuggestions()`

```php
walmartSearchSuggestions($query): mixed
```

Search suggestions

Walmart search-box suggestions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial search term, e.g. 'lapt'

try {
    $result = $apiInstance->walmartSearchSuggestions($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial search term, e.g. &#39;lapt&#39; | |

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

## `walmartWalmartScraperHealthCheck()`

```php
walmartWalmartScraperHealthCheck(): mixed
```

Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->walmartWalmartScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartWalmartScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `walmartWalmartScraperHealthCheckHead()`

```php
walmartWalmartScraperHealthCheckHead(): mixed
```

Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WalmartApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->walmartWalmartScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WalmartApi->walmartWalmartScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

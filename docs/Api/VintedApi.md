# ScrapeBadger\VintedApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**vintedGetItemDetails()**](VintedApi.md#vintedGetItemDetails) | **GET** /v1/vinted/items/{item_id} | Get item details |
| [**vintedGetUserProfile()**](VintedApi.md#vintedGetUserProfile) | **GET** /v1/vinted/users/{user_id} | Get user profile |
| [**vintedGetUserSListedItems()**](VintedApi.md#vintedGetUserSListedItems) | **GET** /v1/vinted/users/{user_id}/items | Get user&#39;s listed items |
| [**vintedListColors()**](VintedApi.md#vintedListColors) | **GET** /v1/vinted/colors | List colors |
| [**vintedListItemConditions()**](VintedApi.md#vintedListItemConditions) | **GET** /v1/vinted/statuses | List item conditions |
| [**vintedListMarkets()**](VintedApi.md#vintedListMarkets) | **GET** /v1/vinted/markets | List markets |
| [**vintedListPublicVintedMobileOperations()**](VintedApi.md#vintedListPublicVintedMobileOperations) | **GET** /v1/vinted/mobile/operations | List public Vinted mobile operations |
| [**vintedReadVintedMobileData()**](VintedApi.md#vintedReadVintedMobileData) | **POST** /v1/vinted/mobile/{operation} | Read Vinted mobile data |
| [**vintedSearchBrands()**](VintedApi.md#vintedSearchBrands) | **GET** /v1/vinted/brands | Search brands |
| [**vintedSearchByImage()**](VintedApi.md#vintedSearchByImage) | **POST** /v1/vinted/search_by_image | Search by image |
| [**vintedSearchVintedItems()**](VintedApi.md#vintedSearchVintedItems) | **GET** /v1/vinted/search | Search Vinted items |
| [**vintedVintedScraperHealthCheck()**](VintedApi.md#vintedVintedScraperHealthCheck) | **GET** /v1/vinted/health | Vinted scraper health check |
| [**vintedVintedScraperHealthCheckHead()**](VintedApi.md#vintedVintedScraperHealthCheckHead) | **HEAD** /v1/vinted/health | Vinted scraper health check |


## `vintedGetItemDetails()`

```php
vintedGetItemDetails($item_id, $market): mixed
```

Get item details

Get detailed information about a Vinted item.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = 56; // int
$market = 'fr'; // string

try {
    $result = $apiInstance->vintedGetItemDetails($item_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedGetItemDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **item_id** | **int**|  | |
| **market** | **string**|  | [optional] [default to &#39;fr&#39;] |

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

## `vintedGetUserProfile()`

```php
vintedGetUserProfile($user_id, $market): mixed
```

Get user profile

Get a Vinted user's profile.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int
$market = 'fr'; // string

try {
    $result = $apiInstance->vintedGetUserProfile($user_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedGetUserProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **int**|  | |
| **market** | **string**|  | [optional] [default to &#39;fr&#39;] |

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

## `vintedGetUserSListedItems()`

```php
vintedGetUserSListedItems($user_id, $market, $page, $per_page): mixed
```

Get user's listed items

Get items listed by a Vinted user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int
$market = 'fr'; // string
$page = 1; // int
$per_page = 20; // int

try {
    $result = $apiInstance->vintedGetUserSListedItems($user_id, $market, $page, $per_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedGetUserSListedItems: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **int**|  | |
| **market** | **string**|  | [optional] [default to &#39;fr&#39;] |
| **page** | **int**|  | [optional] [default to 1] |
| **per_page** | **int**|  | [optional] [default to 20] |

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

## `vintedListColors()`

```php
vintedListColors($market): mixed
```

List colors

Get available Vinted colors for filtering.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$market = 'fr'; // string

try {
    $result = $apiInstance->vintedListColors($market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedListColors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **market** | **string**|  | [optional] [default to &#39;fr&#39;] |

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

## `vintedListItemConditions()`

```php
vintedListItemConditions($market): mixed
```

List item conditions

Get available item condition statuses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$market = 'fr'; // string

try {
    $result = $apiInstance->vintedListItemConditions($market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedListItemConditions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **market** | **string**|  | [optional] [default to &#39;fr&#39;] |

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

## `vintedListMarkets()`

```php
vintedListMarkets(): mixed
```

List markets

List all supported Vinted markets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->vintedListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `vintedListPublicVintedMobileOperations()`

```php
vintedListPublicVintedMobileOperations(): mixed
```

List public Vinted mobile operations

Discover public read operations, parameters and runnable examples. Free.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->vintedListPublicVintedMobileOperations();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedListPublicVintedMobileOperations: ', $e->getMessage(), PHP_EOL;
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

## `vintedReadVintedMobileData()`

```php
vintedReadVintedMobileData($operation, $vinted_mobile_read_request): mixed
```

Read Vinted mobile data

Read catalog, listing, seller, review, sold-comparable, pricing, reference, shipping-reference, homepage or help data. No Vinted account is required. This is an allowlisted read API, including read-only upstream POST queries. Returns operation, market, and the upstream JSON under data. One credit. Sold comparable prices are not guaranteed final negotiated sale prices.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$operation = 'operation_example'; // string
$vinted_mobile_read_request = new \ScrapeBadger\Model\VintedMobileReadRequest(); // \ScrapeBadger\Model\VintedMobileReadRequest

try {
    $result = $apiInstance->vintedReadVintedMobileData($operation, $vinted_mobile_read_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedReadVintedMobileData: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **operation** | **string**|  | |
| **vinted_mobile_read_request** | [**\ScrapeBadger\Model\VintedMobileReadRequest**](../Model/VintedMobileReadRequest.md)|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `vintedSearchBrands()`

```php
vintedSearchBrands($keyword, $market): mixed
```

Search brands

Search Vinted brands.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$keyword = 'keyword_example'; // string | Brand search keyword
$market = 'fr'; // string

try {
    $result = $apiInstance->vintedSearchBrands($keyword, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedSearchBrands: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **keyword** | **string**| Brand search keyword | |
| **market** | **string**|  | [optional] [default to &#39;fr&#39;] |

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

## `vintedSearchByImage()`

```php
vintedSearchByImage($vinted_image_search_request): mixed
```

Search by image

Find active Vinted listings from a photo. 10 credits per successful request. Returns the usual items, pagination and market envelope. Visual ranking. Each item carries `similarity_score` (0-1; the query image's own listing scores 1.0) on the calls where Vinted returns a ranking, and null on the ones where it does not -- a null says nothing about the item. Resend the same image and pagination time for subsequent pages. Structured brand data may be null.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$vinted_image_search_request = new \ScrapeBadger\Model\VintedImageSearchRequest(); // \ScrapeBadger\Model\VintedImageSearchRequest

try {
    $result = $apiInstance->vintedSearchByImage($vinted_image_search_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedSearchByImage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **vinted_image_search_request** | [**\ScrapeBadger\Model\VintedImageSearchRequest**](../Model/VintedImageSearchRequest.md)|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `vintedSearchVintedItems()`

```php
vintedSearchVintedItems($query, $market, $seller_country, $page, $per_page, $price_from, $price_to, $brand_ids, $catalog_ids, $color_ids, $size_ids, $material_ids, $time, $search_session_id, $status_ids, $order): mixed
```

Search Vinted items

Search Vinted catalog items with filters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search text
$market = 'fr'; // string | Market code
$seller_country = 'seller_country_example'; // string | Filter to items whose seller is physically located in one of these comma-separated ISO-2 country codes (e.g. 'fr' or 'fr,be'). Market domains federate cross-border EU listings and Vinted has no native country filter, so each item is enriched with its seller's country and non-matching ones are dropped. Adds 1 credit per uncached seller looked up (cached for 7 days).
$page = 1; // int
$per_page = 20; // int
$price_from = 3.4; // float
$price_to = 3.4; // float
$brand_ids = 'brand_ids_example'; // string
$catalog_ids = 'catalog_ids_example'; // string | Comma-separated Vinted catalog (category) IDs to restrict the search to, e.g. '1904' or '1904,79'. Vinted applies this before searching, so pagination totals reflect the filtered set. A catalog ID is the `catalog[]` value in a Vinted category URL (vinted.fr/catalog?catalog[]=1904).
$color_ids = 'color_ids_example'; // string | Comma-separated color IDs
$size_ids = 'size_ids_example'; // string | Comma-separated size IDs
$material_ids = 'material_ids_example'; // string | Comma-separated material IDs
$time = 56; // int | Pagination time returned by the preceding page
$search_session_id = 'search_session_id_example'; // string | Reuse across pages of one search
$status_ids = 'status_ids_example'; // string | Comma-separated condition/status IDs
$order = 'order_example'; // string

try {
    $result = $apiInstance->vintedSearchVintedItems($query, $market, $seller_country, $page, $per_page, $price_from, $price_to, $brand_ids, $catalog_ids, $color_ids, $size_ids, $material_ids, $time, $search_session_id, $status_ids, $order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedSearchVintedItems: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search text | |
| **market** | **string**| Market code | [optional] [default to &#39;fr&#39;] |
| **seller_country** | **string**| Filter to items whose seller is physically located in one of these comma-separated ISO-2 country codes (e.g. &#39;fr&#39; or &#39;fr,be&#39;). Market domains federate cross-border EU listings and Vinted has no native country filter, so each item is enriched with its seller&#39;s country and non-matching ones are dropped. Adds 1 credit per uncached seller looked up (cached for 7 days). | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **per_page** | **int**|  | [optional] [default to 20] |
| **price_from** | **float**|  | [optional] |
| **price_to** | **float**|  | [optional] |
| **brand_ids** | **string**|  | [optional] |
| **catalog_ids** | **string**| Comma-separated Vinted catalog (category) IDs to restrict the search to, e.g. &#39;1904&#39; or &#39;1904,79&#39;. Vinted applies this before searching, so pagination totals reflect the filtered set. A catalog ID is the &#x60;catalog[]&#x60; value in a Vinted category URL (vinted.fr/catalog?catalog[]&#x3D;1904). | [optional] |
| **color_ids** | **string**| Comma-separated color IDs | [optional] |
| **size_ids** | **string**| Comma-separated size IDs | [optional] |
| **material_ids** | **string**| Comma-separated material IDs | [optional] |
| **time** | **int**| Pagination time returned by the preceding page | [optional] |
| **search_session_id** | **string**| Reuse across pages of one search | [optional] |
| **status_ids** | **string**| Comma-separated condition/status IDs | [optional] |
| **order** | **string**|  | [optional] |

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

## `vintedVintedScraperHealthCheck()`

```php
vintedVintedScraperHealthCheck(): mixed
```

Vinted scraper health check

Check health of the Vinted scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->vintedVintedScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedVintedScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `vintedVintedScraperHealthCheckHead()`

```php
vintedVintedScraperHealthCheckHead(): mixed
```

Vinted scraper health check

Check health of the Vinted scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\VintedApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->vintedVintedScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VintedApi->vintedVintedScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

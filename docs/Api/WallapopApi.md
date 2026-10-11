# ScrapeBadger\WallapopApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**wallapopAutocomplete()**](WallapopApi.md#wallapopAutocomplete) | **GET** /v1/wallapop/autocomplete | Autocomplete |
| [**wallapopGetListingDetail()**](WallapopApi.md#wallapopGetListingDetail) | **GET** /v1/wallapop/items/{item_id} | Get listing detail |
| [**wallapopGetUserListings()**](WallapopApi.md#wallapopGetUserListings) | **GET** /v1/wallapop/users/{user_id}/items | Get user listings |
| [**wallapopGetUserProfile()**](WallapopApi.md#wallapopGetUserProfile) | **GET** /v1/wallapop/users/{user_id} | Get user profile |
| [**wallapopGetUserReviews()**](WallapopApi.md#wallapopGetUserReviews) | **GET** /v1/wallapop/users/{user_id}/reviews | Get user reviews |
| [**wallapopListCategories()**](WallapopApi.md#wallapopListCategories) | **GET** /v1/wallapop/categories | List categories |
| [**wallapopListFilterOptions()**](WallapopApi.md#wallapopListFilterOptions) | **GET** /v1/wallapop/filters/{filter_id}/options | List filter options |
| [**wallapopListMarkets()**](WallapopApi.md#wallapopListMarkets) | **GET** /v1/wallapop/markets | List markets |
| [**wallapopListSearchFilters()**](WallapopApi.md#wallapopListSearchFilters) | **GET** /v1/wallapop/filters | List search filters |
| [**wallapopSearchListings()**](WallapopApi.md#wallapopSearchListings) | **GET** /v1/wallapop/search | Search listings |
| [**wallapopWallapopScraperHealthCheck()**](WallapopApi.md#wallapopWallapopScraperHealthCheck) | **GET** /v1/wallapop/health | Wallapop scraper health check |
| [**wallapopWallapopScraperHealthCheckHead()**](WallapopApi.md#wallapopWallapopScraperHealthCheckHead) | **HEAD** /v1/wallapop/health | Wallapop scraper health check |


## `wallapopAutocomplete()`

```php
wallapopAutocomplete($query, $market): mixed
```

Autocomplete

Wallapop's search-box suggestions for a partial query.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial search text, e.g. 'bici'
$market = 'es'; // string | Market: es (Spain), it (Italy), pt (Portugal)

try {
    $result = $apiInstance->wallapopAutocomplete($query, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopAutocomplete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial search text, e.g. &#39;bici&#39; | |
| **market** | **string**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &#39;es&#39;] |

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

## `wallapopGetListingDetail()`

```php
wallapopGetListingDetail($item_id, $market): mixed
```

Get listing detail

Full listing detail by id (e.g. nzxeknm5x562) or listing slug.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = 'item_id_example'; // string
$market = 'es'; // string | Market: es (Spain), it (Italy), pt (Portugal)

try {
    $result = $apiInstance->wallapopGetListingDetail($item_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopGetListingDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **item_id** | **string**|  | |
| **market** | **string**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &#39;es&#39;] |

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

## `wallapopGetUserListings()`

```php
wallapopGetUserListings($user_id, $market, $next_page): mixed
```

Get user listings

A seller's live listings, 40 per page.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string
$market = 'es'; // string | Market: es (Spain), it (Italy), pt (Portugal)
$next_page = 'next_page_example'; // string | Cursor from the previous page's next_page

try {
    $result = $apiInstance->wallapopGetUserListings($user_id, $market, $next_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopGetUserListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**|  | |
| **market** | **string**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &#39;es&#39;] |
| **next_page** | **string**| Cursor from the previous page&#39;s next_page | [optional] |

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

## `wallapopGetUserProfile()`

```php
wallapopGetUserProfile($user_id, $market): mixed
```

Get user profile

Seller profile with ratings, sales counters, response rate and verifications.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string
$market = 'es'; // string | Market: es (Spain), it (Italy), pt (Portugal)

try {
    $result = $apiInstance->wallapopGetUserProfile($user_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopGetUserProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**|  | |
| **market** | **string**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &#39;es&#39;] |

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

## `wallapopGetUserReviews()`

```php
wallapopGetUserReviews($user_id, $market, $next_page): mixed
```

Get user reviews

Reviews a seller received, newest first, 40 per page.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string
$market = 'es'; // string | Market: es (Spain), it (Italy), pt (Portugal)
$next_page = 'next_page_example'; // string | Cursor from the previous page's next_page

try {
    $result = $apiInstance->wallapopGetUserReviews($user_id, $market, $next_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopGetUserReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**|  | |
| **market** | **string**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &#39;es&#39;] |
| **next_page** | **string**| Cursor from the previous page&#39;s next_page | [optional] |

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

## `wallapopListCategories()`

```php
wallapopListCategories($market): mixed
```

List categories

The full category tree; ids are usable as the search category_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$market = 'es'; // string | Market: es (Spain), it (Italy), pt (Portugal)

try {
    $result = $apiInstance->wallapopListCategories($market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopListCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **market** | **string**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &#39;es&#39;] |

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

## `wallapopListFilterOptions()`

```php
wallapopListFilterOptions($filter_id, $category_id, $query, $market): mixed
```

List filter options

Long option lists (e.g. brand, model) for filters flagged options_endpoint.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$filter_id = 'filter_id_example'; // string
$category_id = 56; // int | Category to scope options to
$query = 'query_example'; // string | Search text to scope options to
$market = 'es'; // string | Market: es (Spain), it (Italy), pt (Portugal)

try {
    $result = $apiInstance->wallapopListFilterOptions($filter_id, $category_id, $query, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopListFilterOptions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **filter_id** | **string**|  | |
| **category_id** | **int**| Category to scope options to | [optional] |
| **query** | **string**| Search text to scope options to | [optional] |
| **market** | **string**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &#39;es&#39;] |

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

## `wallapopListMarkets()`

```php
wallapopListMarkets(): mixed
```

List markets

Supported Wallapop markets and their default search location.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->wallapopListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `wallapopListSearchFilters()`

```php
wallapopListSearchFilters($category_id, $query, $market): mixed
```

List search filters

The filters Wallapop offers for a category or query, with option ids.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = 56; // int | Category the filters apply to
$query = 'query_example'; // string | Search text the filters apply to
$market = 'es'; // string | Market: es (Spain), it (Italy), pt (Portugal)

try {
    $result = $apiInstance->wallapopListSearchFilters($category_id, $query, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopListSearchFilters: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **int**| Category the filters apply to | [optional] |
| **query** | **string**| Search text the filters apply to | [optional] |
| **market** | **string**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &#39;es&#39;] |

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

## `wallapopSearchListings()`

```php
wallapopSearchListings($query, $market, $latitude, $longitude, $distance_km, $category_id, $min_price, $max_price, $condition, $brand, $model, $color, $time_filter, $shippable, $has_warranty, $refurbished, $min_year, $max_year, $min_km, $max_km, $gearbox, $min_horsepower, $max_horsepower, $order_by, $next_page): mixed
```

Search listings

Search Wallapop listings (40 per page). Needs a query, a category_id, or both.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search text, e.g. 'iphone 14'
$market = 'es'; // string | Market: es (Spain), it (Italy), pt (Portugal)
$latitude = 3.4; // float | Search centre latitude (defaults to the market capital)
$longitude = 3.4; // float | Search centre longitude
$distance_km = 56; // int | Search radius
$category_id = 56; // int | Category id from /categories
$min_price = 3.4; // float | Minimum price (EUR)
$max_price = 3.4; // float | Maximum price (EUR)
$condition = 'condition_example'; // string | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all
$brand = 'brand_example'; // string | Brand, e.g. Apple
$model = 'model_example'; // string | Model, e.g. iPhone 14
$color = 'color_example'; // string | Colour id, e.g. black
$time_filter = 'time_filter_example'; // string | Only listings published within this window
$shippable = false; // bool | Only listings that ship
$has_warranty = false; // bool | Only listings with a warranty
$refurbished = false; // bool | Only refurbished listings
$min_year = 56; // int | Cars: earliest model year
$max_year = 56; // int | Cars: latest model year
$min_km = 56; // int | Cars: minimum mileage
$max_km = 56; // int | Cars: maximum mileage
$gearbox = 'gearbox_example'; // string | Cars
$min_horsepower = 56; // int | Cars: minimum power
$max_horsepower = 56; // int | Cars: maximum power
$order_by = 'most_relevance'; // string | Sort order
$next_page = 'next_page_example'; // string | Cursor from the previous page's next_page; other parameters are then ignored

try {
    $result = $apiInstance->wallapopSearchListings($query, $market, $latitude, $longitude, $distance_km, $category_id, $min_price, $max_price, $condition, $brand, $model, $color, $time_filter, $shippable, $has_warranty, $refurbished, $min_year, $max_year, $min_km, $max_km, $gearbox, $min_horsepower, $max_horsepower, $order_by, $next_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopSearchListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search text, e.g. &#39;iphone 14&#39; | [optional] |
| **market** | **string**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &#39;es&#39;] |
| **latitude** | **float**| Search centre latitude (defaults to the market capital) | [optional] |
| **longitude** | **float**| Search centre longitude | [optional] |
| **distance_km** | **int**| Search radius | [optional] |
| **category_id** | **int**| Category id from /categories | [optional] |
| **min_price** | **float**| Minimum price (EUR) | [optional] |
| **max_price** | **float**| Maximum price (EUR) | [optional] |
| **condition** | **string**| Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all | [optional] |
| **brand** | **string**| Brand, e.g. Apple | [optional] |
| **model** | **string**| Model, e.g. iPhone 14 | [optional] |
| **color** | **string**| Colour id, e.g. black | [optional] |
| **time_filter** | **string**| Only listings published within this window | [optional] |
| **shippable** | **bool**| Only listings that ship | [optional] [default to false] |
| **has_warranty** | **bool**| Only listings with a warranty | [optional] [default to false] |
| **refurbished** | **bool**| Only refurbished listings | [optional] [default to false] |
| **min_year** | **int**| Cars: earliest model year | [optional] |
| **max_year** | **int**| Cars: latest model year | [optional] |
| **min_km** | **int**| Cars: minimum mileage | [optional] |
| **max_km** | **int**| Cars: maximum mileage | [optional] |
| **gearbox** | **string**| Cars | [optional] |
| **min_horsepower** | **int**| Cars: minimum power | [optional] |
| **max_horsepower** | **int**| Cars: maximum power | [optional] |
| **order_by** | **string**| Sort order | [optional] [default to &#39;most_relevance&#39;] |
| **next_page** | **string**| Cursor from the previous page&#39;s next_page; other parameters are then ignored | [optional] |

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

## `wallapopWallapopScraperHealthCheck()`

```php
wallapopWallapopScraperHealthCheck(): mixed
```

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->wallapopWallapopScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopWallapopScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `wallapopWallapopScraperHealthCheckHead()`

```php
wallapopWallapopScraperHealthCheckHead(): mixed
```

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\WallapopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->wallapopWallapopScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WallapopApi->wallapopWallapopScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

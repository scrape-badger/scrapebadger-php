# ScrapeBadger\GumtreeApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**gumtreeGetListing()**](GumtreeApi.md#gumtreeGetListing) | **GET** /v1/gumtree/listings/{listing_id} | Get listing |
| [**gumtreeGetSearchFilters()**](GumtreeApi.md#gumtreeGetSearchFilters) | **GET** /v1/gumtree/search/filters | Get search filters |
| [**gumtreeGetSellerListings()**](GumtreeApi.md#gumtreeGetSellerListings) | **GET** /v1/gumtree/listings/{listing_id}/seller-listings | Get seller listings |
| [**gumtreeGumtreeScraperHealthCheck()**](GumtreeApi.md#gumtreeGumtreeScraperHealthCheck) | **GET** /v1/gumtree/health | Gumtree scraper health check |
| [**gumtreeGumtreeScraperHealthCheckHead()**](GumtreeApi.md#gumtreeGumtreeScraperHealthCheckHead) | **HEAD** /v1/gumtree/health | Gumtree scraper health check |
| [**gumtreeListCategories()**](GumtreeApi.md#gumtreeListCategories) | **GET** /v1/gumtree/categories | List categories |
| [**gumtreeListLocations()**](GumtreeApi.md#gumtreeListLocations) | **GET** /v1/gumtree/locations | List locations |
| [**gumtreeLocationSuggestions()**](GumtreeApi.md#gumtreeLocationSuggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions |
| [**gumtreeSearchListings()**](GumtreeApi.md#gumtreeSearchListings) | **GET** /v1/gumtree/search | Search listings |
| [**gumtreeSearchSuggestions()**](GumtreeApi.md#gumtreeSearchSuggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions |


## `gumtreeGetListing()`

```php
gumtreeGetListing($listing_id): mixed
```

Get listing

Full listing — description, attributes, images, seller, similar listings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GumtreeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$listing_id = 'listing_id_example'; // string | Gumtree listing id — the number at the end of a gumtree.com/p/... URL

try {
    $result = $apiInstance->gumtreeGetListing($listing_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GumtreeApi->gumtreeGetListing: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **listing_id** | **string**| Gumtree listing id — the number at the end of a gumtree.com/p/... URL | |

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

## `gumtreeGetSearchFilters()`

```php
gumtreeGetSearchFilters($category, $location, $query): mixed
```

Get search filters

Filters, sort orders and radius options for a category, with live counts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GumtreeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category = 'all'; // string | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'.
$location = 'uk'; // string | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'.
$query = 'query_example'; // string

try {
    $result = $apiInstance->gumtreeGetSearchFilters($category, $location, $query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GumtreeApi->gumtreeGetSearchFilters: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category** | **string**| Category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;. Default &#39;all&#39;. | [optional] [default to &#39;all&#39;] |
| **location** | **string**| Location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). Default &#39;uk&#39;. | [optional] [default to &#39;uk&#39;] |
| **query** | **string**|  | [optional] |

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

## `gumtreeGetSellerListings()`

```php
gumtreeGetSellerListings($listing_id, $page): mixed
```

Get seller listings

Every live listing by the seller of the given listing.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GumtreeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$listing_id = 'listing_id_example'; // string | Gumtree listing id — the number at the end of a gumtree.com/p/... URL
$page = 1; // int

try {
    $result = $apiInstance->gumtreeGetSellerListings($listing_id, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GumtreeApi->gumtreeGetSellerListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **listing_id** | **string**| Gumtree listing id — the number at the end of a gumtree.com/p/... URL | |
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

## `gumtreeGumtreeScraperHealthCheck()`

```php
gumtreeGumtreeScraperHealthCheck(): mixed
```

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GumtreeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->gumtreeGumtreeScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GumtreeApi->gumtreeGumtreeScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `gumtreeGumtreeScraperHealthCheckHead()`

```php
gumtreeGumtreeScraperHealthCheckHead(): mixed
```

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GumtreeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->gumtreeGumtreeScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GumtreeApi->gumtreeGumtreeScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `gumtreeListCategories()`

```php
gumtreeListCategories($parent_id): mixed
```

List categories

Browse Gumtree's category tree. A node's `slug` is the `/search` category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GumtreeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$parent_id = 1; // int | Parent category id (default: all)

try {
    $result = $apiInstance->gumtreeListCategories($parent_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GumtreeApi->gumtreeListCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **parent_id** | **int**| Parent category id (default: all) | [optional] [default to 1] |

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

## `gumtreeListLocations()`

```php
gumtreeListLocations($parent_id): mixed
```

List locations

Browse Gumtree's location tree.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GumtreeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$parent_id = 10000392; // int | Parent location id (default: UK)

try {
    $result = $apiInstance->gumtreeListLocations($parent_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GumtreeApi->gumtreeListLocations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **parent_id** | **int**| Parent location id (default: UK) | [optional] [default to 10000392] |

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

## `gumtreeLocationSuggestions()`

```php
gumtreeLocationSuggestions($query): mixed
```

Location suggestions

Resolve a place name or postcode to Gumtree locations with coordinates.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GumtreeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Town or postcode prefix, e.g. 'manch'

try {
    $result = $apiInstance->gumtreeLocationSuggestions($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GumtreeApi->gumtreeLocationSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Town or postcode prefix, e.g. &#39;manch&#39; | |

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

## `gumtreeSearchListings()`

```php
gumtreeSearchListings($query, $category, $location, $distance, $min_price, $max_price, $sort, $seller_type, $urgent_only, $with_photos, $filters, $page): mixed
```

Search listings

Search gumtree.com listings. ~25-30 per page, up to 50 pages.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GumtreeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'mountain bike'
$category = 'all'; // string | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'.
$location = 'uk'; // string | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'.
$distance = 3.4; // float | Radius in miles
$min_price = 56; // int | GBP; needs a category
$max_price = 56; // int | GBP; needs a category
$sort = 'sort_example'; // string
$seller_type = 'seller_type_example'; // string
$urgent_only = false; // bool
$with_photos = false; // bool
$filters = 'filters_example'; // string | Category filters as key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol'
$page = 1; // int

try {
    $result = $apiInstance->gumtreeSearchListings($query, $category, $location, $distance, $min_price, $max_price, $sort, $seller_type, $urgent_only, $with_photos, $filters, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GumtreeApi->gumtreeSearchListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;mountain bike&#39; | [optional] |
| **category** | **string**| Category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;. Default &#39;all&#39;. | [optional] [default to &#39;all&#39;] |
| **location** | **string**| Location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). Default &#39;uk&#39;. | [optional] [default to &#39;uk&#39;] |
| **distance** | **float**| Radius in miles | [optional] |
| **min_price** | **int**| GBP; needs a category | [optional] |
| **max_price** | **int**| GBP; needs a category | [optional] |
| **sort** | **string**|  | [optional] |
| **seller_type** | **string**|  | [optional] |
| **urgent_only** | **bool**|  | [optional] [default to false] |
| **with_photos** | **bool**|  | [optional] [default to false] |
| **filters** | **string**| Category filters as key:value pairs, e.g. &#39;vehicle_make:bmw,vehicle_fuel_type:petrol&#39; | [optional] |
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

## `gumtreeSearchSuggestions()`

```php
gumtreeSearchSuggestions($query): mixed
```

Search suggestions

Gumtree search-box keyword suggestions with their categories.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GumtreeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial search term, e.g. 'iph'

try {
    $result = $apiInstance->gumtreeSearchSuggestions($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GumtreeApi->gumtreeSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial search term, e.g. &#39;iph&#39; | |

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

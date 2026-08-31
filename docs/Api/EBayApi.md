# ScrapeBadger\EBayApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**ebayBrowseACategory()**](EBayApi.md#ebayBrowseACategory) | **GET** /v1/ebay/categories/{category_id}/items | Browse a category |
| [**ebayCompletedSoldListings()**](EBayApi.md#ebayCompletedSoldListings) | **GET** /v1/ebay/completed | Completed / sold listings |
| [**ebayEbayScraperHealthCheck()**](EBayApi.md#ebayEbayScraperHealthCheck) | **GET** /v1/ebay/health | eBay scraper health check |
| [**ebayEbayScraperHealthCheckHead()**](EBayApi.md#ebayEbayScraperHealthCheckHead) | **HEAD** /v1/ebay/health | eBay scraper health check |
| [**ebayGetItemDetail()**](EBayApi.md#ebayGetItemDetail) | **GET** /v1/ebay/items/{item_id} | Get item detail |
| [**ebayGetItemReviews()**](EBayApi.md#ebayGetItemReviews) | **GET** /v1/ebay/items/{item_id}/reviews | Get item reviews |
| [**ebayGetSellerFeedback()**](EBayApi.md#ebayGetSellerFeedback) | **GET** /v1/ebay/sellers/{username}/feedback | Get seller feedback |
| [**ebayGetSellerListings()**](EBayApi.md#ebayGetSellerListings) | **GET** /v1/ebay/sellers/{username}/items | Get seller listings |
| [**ebayGetSellerProfile()**](EBayApi.md#ebayGetSellerProfile) | **GET** /v1/ebay/sellers/{username} | Get seller profile |
| [**ebayKeywordSuggestions()**](EBayApi.md#ebayKeywordSuggestions) | **GET** /v1/ebay/autocomplete | Keyword suggestions |
| [**ebayListCategories()**](EBayApi.md#ebayListCategories) | **GET** /v1/ebay/categories | List categories |
| [**ebayListMarkets()**](EBayApi.md#ebayListMarkets) | **GET** /v1/ebay/markets | List markets |
| [**ebaySearchListings()**](EBayApi.md#ebaySearchListings) | **GET** /v1/ebay/search | Search listings |


## `ebayBrowseACategory()`

```php
ebayBrowseACategory($category_id, $domain, $page, $per_page, $sort_by, $min_price, $max_price): mixed
```

Browse a category

List active listings within an eBay category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = 'category_id_example'; // string
$domain = 'com'; // string
$page = 1; // int
$per_page = 56; // int
$sort_by = 'best_match'; // string | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
$min_price = 3.4; // float
$max_price = 3.4; // float

try {
    $result = $apiInstance->ebayBrowseACategory($category_id, $domain, $page, $per_page, $sort_by, $min_price, $max_price);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayBrowseACategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **string**|  | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
| **page** | **int**|  | [optional] [default to 1] |
| **per_page** | **int**|  | [optional] |
| **sort_by** | **string**| best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to &#39;best_match&#39;] |
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

## `ebayCompletedSoldListings()`

```php
ebayCompletedSoldListings($query, $domain, $category_id, $page, $per_page, $sort_by, $condition, $min_price, $max_price, $location): mixed
```

Completed / sold listings

Search completed/sold listings — eBay's sold-price history.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords
$domain = 'com'; // string | Marketplace domain (com, co.uk, de …)
$category_id = 'category_id_example'; // string | Restrict to a category id
$page = 1; // int
$per_page = 56; // int | 60, 120 or 240
$sort_by = 'best_match'; // string | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
$condition = 'condition_example'; // string | new|open_box|refurbished|used|for_parts|graded|ungraded
$min_price = 3.4; // float
$max_price = 3.4; // float
$location = 'location_example'; // string | domestic|worldwide

try {
    $result = $apiInstance->ebayCompletedSoldListings($query, $domain, $category_id, $page, $per_page, $sort_by, $condition, $min_price, $max_price, $location);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayCompletedSoldListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords | |
| **domain** | **string**| Marketplace domain (com, co.uk, de …) | [optional] [default to &#39;com&#39;] |
| **category_id** | **string**| Restrict to a category id | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **per_page** | **int**| 60, 120 or 240 | [optional] |
| **sort_by** | **string**| best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to &#39;best_match&#39;] |
| **condition** | **string**| new|open_box|refurbished|used|for_parts|graded|ungraded | [optional] |
| **min_price** | **float**|  | [optional] |
| **max_price** | **float**|  | [optional] |
| **location** | **string**| domestic|worldwide | [optional] |

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

## `ebayEbayScraperHealthCheck()`

```php
ebayEbayScraperHealthCheck(): mixed
```

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->ebayEbayScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayEbayScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `ebayEbayScraperHealthCheckHead()`

```php
ebayEbayScraperHealthCheckHead(): mixed
```

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->ebayEbayScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayEbayScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `ebayGetItemDetail()`

```php
ebayGetItemDetail($item_id, $domain): mixed
```

Get item detail

Get a single eBay listing's full detail.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = 'item_id_example'; // string
$domain = 'com'; // string

try {
    $result = $apiInstance->ebayGetItemDetail($item_id, $domain);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayGetItemDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **item_id** | **string**|  | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |

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

## `ebayGetItemReviews()`

```php
ebayGetItemReviews($item_id, $domain, $page): mixed
```

Get item reviews

Get catalog product reviews shown on an eBay listing.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = 'item_id_example'; // string
$domain = 'com'; // string
$page = 1; // int

try {
    $result = $apiInstance->ebayGetItemReviews($item_id, $domain, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayGetItemReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **item_id** | **string**|  | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
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

## `ebayGetSellerFeedback()`

```php
ebayGetSellerFeedback($username, $domain, $page): mixed
```

Get seller feedback

Get a seller's recent feedback comments.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$domain = 'com'; // string
$page = 1; // int

try {
    $result = $apiInstance->ebayGetSellerFeedback($username, $domain, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayGetSellerFeedback: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
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

## `ebayGetSellerListings()`

```php
ebayGetSellerListings($username, $domain, $query, $page, $per_page): mixed
```

Get seller listings

List the active listings of a single eBay seller.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$domain = 'com'; // string
$query = 'query_example'; // string
$page = 1; // int
$per_page = 56; // int

try {
    $result = $apiInstance->ebayGetSellerListings($username, $domain, $query, $page, $per_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayGetSellerListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
| **query** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **per_page** | **int**|  | [optional] |

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

## `ebayGetSellerProfile()`

```php
ebayGetSellerProfile($username, $domain): mixed
```

Get seller profile

Get an eBay seller's public profile.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$domain = 'com'; // string

try {
    $result = $apiInstance->ebayGetSellerProfile($username, $domain);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayGetSellerProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |

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

## `ebayKeywordSuggestions()`

```php
ebayKeywordSuggestions($query, $domain): mixed
```

Keyword suggestions

Return eBay keyword autocomplete suggestions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial query prefix
$domain = 'com'; // string

try {
    $result = $apiInstance->ebayKeywordSuggestions($query, $domain);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayKeywordSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial query prefix | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |

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

## `ebayListCategories()`

```php
ebayListCategories(): mixed
```

List categories

List eBay's top-level category ids.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->ebayListCategories();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayListCategories: ', $e->getMessage(), PHP_EOL;
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

## `ebayListMarkets()`

```php
ebayListMarkets(): mixed
```

List markets

List all supported eBay marketplaces.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->ebayListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebayListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `ebaySearchListings()`

```php
ebaySearchListings($query, $domain, $category_id, $page, $per_page, $sort_by, $condition, $buying_format, $min_price, $max_price, $free_shipping, $location): mixed
```

Search listings

Search an eBay marketplace for active listings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EBayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords
$domain = 'com'; // string | Marketplace domain (com, co.uk, de …)
$category_id = 'category_id_example'; // string | Restrict to a category id
$page = 1; // int
$per_page = 56; // int | 60, 120 or 240
$sort_by = 'best_match'; // string | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
$condition = 'condition_example'; // string | new|open_box|refurbished|used|for_parts|graded|ungraded
$buying_format = 'buying_format_example'; // string | auction|buy_it_now|best_offer
$min_price = 3.4; // float
$max_price = 3.4; // float
$free_shipping = false; // bool
$location = 'location_example'; // string | domestic|worldwide

try {
    $result = $apiInstance->ebaySearchListings($query, $domain, $category_id, $page, $per_page, $sort_by, $condition, $buying_format, $min_price, $max_price, $free_shipping, $location);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EBayApi->ebaySearchListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords | |
| **domain** | **string**| Marketplace domain (com, co.uk, de …) | [optional] [default to &#39;com&#39;] |
| **category_id** | **string**| Restrict to a category id | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **per_page** | **int**| 60, 120 or 240 | [optional] |
| **sort_by** | **string**| best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to &#39;best_match&#39;] |
| **condition** | **string**| new|open_box|refurbished|used|for_parts|graded|ungraded | [optional] |
| **buying_format** | **string**| auction|buy_it_now|best_offer | [optional] |
| **min_price** | **float**|  | [optional] |
| **max_price** | **float**|  | [optional] |
| **free_shipping** | **bool**|  | [optional] [default to false] |
| **location** | **string**| domestic|worldwide | [optional] |

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

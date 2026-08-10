# ScrapeBadger\AmazonApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**amazonAmazonScraperHealthCheck()**](AmazonApi.md#amazonAmazonScraperHealthCheck) | **GET** /v1/amazon/health | Amazon scraper health check |
| [**amazonAmazonScraperHealthCheckHead()**](AmazonApi.md#amazonAmazonScraperHealthCheckHead) | **HEAD** /v1/amazon/health | Amazon scraper health check |
| [**amazonBestsellersByCategory()**](AmazonApi.md#amazonBestsellersByCategory) | **GET** /v1/amazon/bestsellers | Bestsellers by category |
| [**amazonBrowseNodeCategoryListing()**](AmazonApi.md#amazonBrowseNodeCategoryListing) | **GET** /v1/amazon/category | Browse-node category listing |
| [**amazonGetAllSellerOffersBuybox()**](AmazonApi.md#amazonGetAllSellerOffersBuybox) | **GET** /v1/amazon/products/{asin}/offers | Get all seller offers (buybox) |
| [**amazonGetProductDetail()**](AmazonApi.md#amazonGetProductDetail) | **GET** /v1/amazon/products/{asin} | Get product detail |
| [**amazonGetProductReviews()**](AmazonApi.md#amazonGetProductReviews) | **GET** /v1/amazon/products/{asin}/reviews | Get product reviews |
| [**amazonGetSellerFeedback()**](AmazonApi.md#amazonGetSellerFeedback) | **GET** /v1/amazon/sellers/{seller_id}/feedback | Get seller feedback |
| [**amazonGetSellerProfile()**](AmazonApi.md#amazonGetSellerProfile) | **GET** /v1/amazon/sellers/{seller_id} | Get seller profile |
| [**amazonGetSellerStorefrontProducts()**](AmazonApi.md#amazonGetSellerStorefrontProducts) | **GET** /v1/amazon/sellers/{seller_id}/products | Get seller storefront products |
| [**amazonKeywordSuggestions()**](AmazonApi.md#amazonKeywordSuggestions) | **GET** /v1/amazon/autocomplete | Keyword suggestions |
| [**amazonListCategoryAliases()**](AmazonApi.md#amazonListCategoryAliases) | **GET** /v1/amazon/categories | List category aliases |
| [**amazonListMarketplaces()**](AmazonApi.md#amazonListMarketplaces) | **GET** /v1/amazon/markets | List marketplaces |
| [**amazonNewReleasesByCategory()**](AmazonApi.md#amazonNewReleasesByCategory) | **GET** /v1/amazon/new-releases | New releases by category |
| [**amazonSearchAmazonProducts()**](AmazonApi.md#amazonSearchAmazonProducts) | **GET** /v1/amazon/search | Search Amazon products |
| [**amazonTodaySDeals()**](AmazonApi.md#amazonTodaySDeals) | **GET** /v1/amazon/deals | Today&#39;s deals |


## `amazonAmazonScraperHealthCheck()`

```php
amazonAmazonScraperHealthCheck(): mixed
```

Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->amazonAmazonScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonAmazonScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `amazonAmazonScraperHealthCheckHead()`

```php
amazonAmazonScraperHealthCheckHead(): mixed
```

Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->amazonAmazonScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonAmazonScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `amazonBestsellersByCategory()`

```php
amazonBestsellersByCategory($domain, $category, $page): mixed
```

Bestsellers by category

Top-selling products for a category (browse node).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'com'; // string
$category = 'category_example'; // string | Bestsellers node id or slug
$page = 1; // int

try {
    $result = $apiInstance->amazonBestsellersByCategory($domain, $category, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonBestsellersByCategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
| **category** | **string**| Bestsellers node id or slug | [optional] |
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

## `amazonBrowseNodeCategoryListing()`

```php
amazonBrowseNodeCategoryListing($node, $domain, $page, $sort_by): mixed
```

Browse-node category listing

List products within an Amazon browse-node category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$node = 'node_example'; // string | Amazon browse-node id
$domain = 'com'; // string
$page = 1; // int
$sort_by = 'sort_by_example'; // string

try {
    $result = $apiInstance->amazonBrowseNodeCategoryListing($node, $domain, $page, $sort_by);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonBrowseNodeCategoryListing: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **node** | **string**| Amazon browse-node id | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
| **page** | **int**|  | [optional] [default to 1] |
| **sort_by** | **string**|  | [optional] |

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

## `amazonGetAllSellerOffersBuybox()`

```php
amazonGetAllSellerOffersBuybox($asin, $domain, $zip): mixed
```

Get all seller offers (buybox)

All third-party offers for an ASIN, including the Buy Box winner.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$asin = 'asin_example'; // string
$domain = 'com'; // string
$zip = 'zip_example'; // string

try {
    $result = $apiInstance->amazonGetAllSellerOffersBuybox($asin, $domain, $zip);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonGetAllSellerOffersBuybox: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **asin** | **string**|  | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
| **zip** | **string**|  | [optional] |

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

## `amazonGetProductDetail()`

```php
amazonGetProductDetail($asin, $domain, $zip, $language): mixed
```

Get product detail

Full product detail by ASIN (price, variants, badges, buybox, ranks…).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$asin = 'asin_example'; // string
$domain = 'com'; // string
$zip = 'zip_example'; // string | Delivery postal/zip for localized buybox
$language = 'language_example'; // string

try {
    $result = $apiInstance->amazonGetProductDetail($asin, $domain, $zip, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonGetProductDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **asin** | **string**|  | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
| **zip** | **string**| Delivery postal/zip for localized buybox | [optional] |
| **language** | **string**|  | [optional] |

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

## `amazonGetProductReviews()`

```php
amazonGetProductReviews($asin, $domain, $page, $sort_by, $star, $verified_only, $media_only): mixed
```

Get product reviews

Customer reviews for an ASIN (featured + paginated, with filters).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$asin = 'asin_example'; // string
$domain = 'com'; // string
$page = 1; // int | Review page (1-100, ~10 reviews/page)
$sort_by = 'helpful'; // string | helpful | recent
$star = 'star_example'; // string | one_star..five_star | positive | critical
$verified_only = false; // bool
$media_only = false; // bool

try {
    $result = $apiInstance->amazonGetProductReviews($asin, $domain, $page, $sort_by, $star, $verified_only, $media_only);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonGetProductReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **asin** | **string**|  | |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
| **page** | **int**| Review page (1-100, ~10 reviews/page) | [optional] [default to 1] |
| **sort_by** | **string**| helpful | recent | [optional] [default to &#39;helpful&#39;] |
| **star** | **string**| one_star..five_star | positive | critical | [optional] |
| **verified_only** | **bool**|  | [optional] [default to false] |
| **media_only** | **bool**|  | [optional] [default to false] |

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

## `amazonGetSellerFeedback()`

```php
amazonGetSellerFeedback($seller_id, $domain, $page): mixed
```

Get seller feedback

Buyer feedback entries for a seller.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$seller_id = 'seller_id_example'; // string
$domain = 'com'; // string
$page = 1; // int

try {
    $result = $apiInstance->amazonGetSellerFeedback($seller_id, $domain, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonGetSellerFeedback: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **seller_id** | **string**|  | |
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

## `amazonGetSellerProfile()`

```php
amazonGetSellerProfile($seller_id, $domain): mixed
```

Get seller profile

Seller profile, ratings and feedback summary.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$seller_id = 'seller_id_example'; // string
$domain = 'com'; // string

try {
    $result = $apiInstance->amazonGetSellerProfile($seller_id, $domain);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonGetSellerProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **seller_id** | **string**|  | |
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

## `amazonGetSellerStorefrontProducts()`

```php
amazonGetSellerStorefrontProducts($seller_id, $domain, $page): mixed
```

Get seller storefront products

Products listed in a seller's storefront.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$seller_id = 'seller_id_example'; // string
$domain = 'com'; // string
$page = 1; // int

try {
    $result = $apiInstance->amazonGetSellerStorefrontProducts($seller_id, $domain, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonGetSellerStorefrontProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **seller_id** | **string**|  | |
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

## `amazonKeywordSuggestions()`

```php
amazonKeywordSuggestions($query, $domain): mixed
```

Keyword suggestions

Get Amazon search autocomplete suggestions for keyword research.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial search term
$domain = 'com'; // string

try {
    $result = $apiInstance->amazonKeywordSuggestions($query, $domain);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonKeywordSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial search term | |
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

## `amazonListCategoryAliases()`

```php
amazonListCategoryAliases($domain): mixed
```

List category aliases

List common Amazon department/category aliases and bestseller nodes.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'com'; // string

try {
    $result = $apiInstance->amazonListCategoryAliases($domain);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonListCategoryAliases: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `amazonListMarketplaces()`

```php
amazonListMarketplaces(): mixed
```

List marketplaces

List all supported Amazon marketplaces.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->amazonListMarketplaces();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonListMarketplaces: ', $e->getMessage(), PHP_EOL;
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

## `amazonNewReleasesByCategory()`

```php
amazonNewReleasesByCategory($domain, $category, $page): mixed
```

New releases by category

Newly released products for a category (browse node).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'com'; // string
$category = 'category_example'; // string
$page = 1; // int

try {
    $result = $apiInstance->amazonNewReleasesByCategory($domain, $category, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonNewReleasesByCategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
| **category** | **string**|  | [optional] |
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

## `amazonSearchAmazonProducts()`

```php
amazonSearchAmazonProducts($query, $domain, $page, $sort_by, $category, $min_price, $max_price, $zip, $language): mixed
```

Search Amazon products

Search the Amazon catalog with filters and sorting.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords
$domain = 'com'; // string | Amazon marketplace TLD or code (com, co.uk, de…)
$page = 1; // int
$sort_by = 'sort_by_example'; // string | relevance | price_low_to_high | price_high_to_low | avg_review | newest
$category = 'category_example'; // string | Department/category alias (i= param)
$min_price = 3.4; // float
$max_price = 3.4; // float
$zip = 'zip_example'; // string | Delivery postal/zip code for localized pricing
$language = 'language_example'; // string | Locale for results, e.g. en_US, fr_FR

try {
    $result = $apiInstance->amazonSearchAmazonProducts($query, $domain, $page, $sort_by, $category, $min_price, $max_price, $zip, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonSearchAmazonProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords | |
| **domain** | **string**| Amazon marketplace TLD or code (com, co.uk, de…) | [optional] [default to &#39;com&#39;] |
| **page** | **int**|  | [optional] [default to 1] |
| **sort_by** | **string**| relevance | price_low_to_high | price_high_to_low | avg_review | newest | [optional] |
| **category** | **string**| Department/category alias (i&#x3D; param) | [optional] |
| **min_price** | **float**|  | [optional] |
| **max_price** | **float**|  | [optional] |
| **zip** | **string**| Delivery postal/zip code for localized pricing | [optional] |
| **language** | **string**| Locale for results, e.g. en_US, fr_FR | [optional] |

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

## `amazonTodaySDeals()`

```php
amazonTodaySDeals($domain, $category, $page): mixed
```

Today's deals

Current Amazon deals (lightning deals, best deals).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AmazonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain = 'com'; // string
$category = 'category_example'; // string
$page = 1; // int

try {
    $result = $apiInstance->amazonTodaySDeals($domain, $category, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AmazonApi->amazonTodaySDeals: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain** | **string**|  | [optional] [default to &#39;com&#39;] |
| **category** | **string**|  | [optional] |
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

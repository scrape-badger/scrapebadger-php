# ScrapeBadger\EtsyApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**etsyGetCategories()**](EtsyApi.md#etsyGetCategories) | **GET** /v1/etsy/categories | Get categories |
| [**etsyGetListingDetail()**](EtsyApi.md#etsyGetListingDetail) | **GET** /v1/etsy/listings/{listing_id} | Get listing detail |
| [**etsyGetListingReviews()**](EtsyApi.md#etsyGetListingReviews) | **GET** /v1/etsy/listings/{listing_id}/reviews | Get listing reviews |
| [**etsyGetSearchSuggestions()**](EtsyApi.md#etsyGetSearchSuggestions) | **GET** /v1/etsy/autocomplete | Get search suggestions |
| [**etsyGetShopListings()**](EtsyApi.md#etsyGetShopListings) | **GET** /v1/etsy/shops/{shop_name}/listings | Get shop listings |
| [**etsyGetShopProfile()**](EtsyApi.md#etsyGetShopProfile) | **GET** /v1/etsy/shops/{shop_name} | Get shop profile |
| [**etsyGetShopReviews()**](EtsyApi.md#etsyGetShopReviews) | **GET** /v1/etsy/shops/{shop_name}/reviews | Get shop reviews |
| [**etsySearchListings()**](EtsyApi.md#etsySearchListings) | **GET** /v1/etsy/search | Search listings |


## `etsyGetCategories()`

```php
etsyGetCategories($country, $currency, $language): mixed
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


$apiInstance = new ScrapeBadger\Api\EtsyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en-US'; // string

try {
    $result = $apiInstance->etsyGetCategories($country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EtsyApi->etsyGetCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en-US&#39;] |

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

## `etsyGetListingDetail()`

```php
etsyGetListingDetail($listing_id, $country, $currency, $language): mixed
```

Get listing detail

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EtsyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$listing_id = 'listing_id_example'; // string
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en-US'; // string

try {
    $result = $apiInstance->etsyGetListingDetail($listing_id, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EtsyApi->etsyGetListingDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **listing_id** | **string**|  | |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en-US&#39;] |

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

## `etsyGetListingReviews()`

```php
etsyGetListingReviews($listing_id, $page, $sort, $country, $currency, $language): mixed
```

Get listing reviews

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EtsyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$listing_id = 'listing_id_example'; // string
$page = 1; // int
$sort = 'Relevancy'; // string
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en-US'; // string

try {
    $result = $apiInstance->etsyGetListingReviews($listing_id, $page, $sort, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EtsyApi->etsyGetListingReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **listing_id** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **sort** | **string**|  | [optional] [default to &#39;Relevancy&#39;] |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en-US&#39;] |

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

## `etsyGetSearchSuggestions()`

```php
etsyGetSearchSuggestions($query, $country, $currency, $language): mixed
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


$apiInstance = new ScrapeBadger\Api\EtsyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en-US'; // string

try {
    $result = $apiInstance->etsyGetSearchSuggestions($query, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EtsyApi->etsyGetSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en-US&#39;] |

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

## `etsyGetShopListings()`

```php
etsyGetShopListings($shop_name, $page, $country, $currency, $language): mixed
```

Get shop listings

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EtsyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shop_name = 'shop_name_example'; // string
$page = 1; // int
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en-US'; // string

try {
    $result = $apiInstance->etsyGetShopListings($shop_name, $page, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EtsyApi->etsyGetShopListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shop_name** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en-US&#39;] |

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

## `etsyGetShopProfile()`

```php
etsyGetShopProfile($shop_name, $country, $currency, $language): mixed
```

Get shop profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EtsyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shop_name = 'shop_name_example'; // string
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en-US'; // string

try {
    $result = $apiInstance->etsyGetShopProfile($shop_name, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EtsyApi->etsyGetShopProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shop_name** | **string**|  | |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en-US&#39;] |

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

## `etsyGetShopReviews()`

```php
etsyGetShopReviews($shop_name, $page, $country, $currency, $language): mixed
```

Get shop reviews

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EtsyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shop_name = 'shop_name_example'; // string
$page = 1; // int
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en-US'; // string

try {
    $result = $apiInstance->etsyGetShopReviews($shop_name, $page, $country, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EtsyApi->etsyGetShopReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shop_name** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en-US&#39;] |

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

## `etsySearchListings()`

```php
etsySearchListings($query, $page, $country, $currency, $language, $sort, $min_price, $max_price): mixed
```

Search listings

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\EtsyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$page = 1; // int
$country = 'US'; // string
$currency = 'USD'; // string
$language = 'en-US'; // string
$sort = 'most_relevant'; // string
$min_price = 3.4; // float
$max_price = 3.4; // float

try {
    $result = $apiInstance->etsySearchListings($query, $page, $country, $currency, $language, $sort, $min_price, $max_price);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EtsyApi->etsySearchListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en-US&#39;] |
| **sort** | **string**|  | [optional] [default to &#39;most_relevant&#39;] |
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

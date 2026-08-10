# ScrapeBadger\LeboncoinApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**leboncoinGetASellerSAds()**](LeboncoinApi.md#leboncoinGetASellerSAds) | **GET** /v1/leboncoin/sellers/{user_id}/listings | Get a seller&#39;s ads |
| [**leboncoinGetAdDetail()**](LeboncoinApi.md#leboncoinGetAdDetail) | **GET** /v1/leboncoin/ads/{list_id} | Get ad detail |
| [**leboncoinGetSellerProfile()**](LeboncoinApi.md#leboncoinGetSellerProfile) | **GET** /v1/leboncoin/sellers/{user_id} | Get seller profile |
| [**leboncoinGetSimilarAds()**](LeboncoinApi.md#leboncoinGetSimilarAds) | **GET** /v1/leboncoin/ads/{list_id}/similar | Get similar ads |
| [**leboncoinLeboncoinScraperHealthCheck()**](LeboncoinApi.md#leboncoinLeboncoinScraperHealthCheck) | **GET** /v1/leboncoin/health | Leboncoin scraper health check |
| [**leboncoinLeboncoinScraperHealthCheckHead()**](LeboncoinApi.md#leboncoinLeboncoinScraperHealthCheckHead) | **HEAD** /v1/leboncoin/health | Leboncoin scraper health check |
| [**leboncoinListCategories()**](LeboncoinApi.md#leboncoinListCategories) | **GET** /v1/leboncoin/categories | List categories |
| [**leboncoinListDepartments()**](LeboncoinApi.md#leboncoinListDepartments) | **GET** /v1/leboncoin/departments | List departments |
| [**leboncoinListMarkets()**](LeboncoinApi.md#leboncoinListMarkets) | **GET** /v1/leboncoin/markets | List markets |
| [**leboncoinListRegions()**](LeboncoinApi.md#leboncoinListRegions) | **GET** /v1/leboncoin/regions | List regions |
| [**leboncoinLocationAutocomplete()**](LeboncoinApi.md#leboncoinLocationAutocomplete) | **GET** /v1/leboncoin/locations/search | Location autocomplete |
| [**leboncoinSearchLeboncoinAds()**](LeboncoinApi.md#leboncoinSearchLeboncoinAds) | **GET** /v1/leboncoin/search | Search Leboncoin ads |


## `leboncoinGetASellerSAds()`

```php
leboncoinGetASellerSAds($user_id, $page, $limit): mixed
```

Get a seller's ads

A seller's active ads.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string
$page = 1; // int
$limit = 35; // int

try {
    $result = $apiInstance->leboncoinGetASellerSAds($user_id, $page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinGetASellerSAds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **limit** | **int**|  | [optional] [default to 35] |

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

## `leboncoinGetAdDetail()`

```php
leboncoinGetAdDetail($list_id): mixed
```

Get ad detail

Full detail for a Leboncoin ad.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$list_id = 56; // int

try {
    $result = $apiInstance->leboncoinGetAdDetail($list_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinGetAdDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **list_id** | **int**|  | |

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

## `leboncoinGetSellerProfile()`

```php
leboncoinGetSellerProfile($user_id): mixed
```

Get seller profile

Public seller/pro-store profile.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string

try {
    $result = $apiInstance->leboncoinGetSellerProfile($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinGetSellerProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**|  | |

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

## `leboncoinGetSimilarAds()`

```php
leboncoinGetSimilarAds($list_id, $limit): mixed
```

Get similar ads

Ads Leboncoin surfaces as similar to the given ad.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$list_id = 56; // int
$limit = 20; // int

try {
    $result = $apiInstance->leboncoinGetSimilarAds($list_id, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinGetSimilarAds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **list_id** | **int**|  | |
| **limit** | **int**|  | [optional] [default to 20] |

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

## `leboncoinLeboncoinScraperHealthCheck()`

```php
leboncoinLeboncoinScraperHealthCheck(): mixed
```

Leboncoin scraper health check

Check health of the Leboncoin scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->leboncoinLeboncoinScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinLeboncoinScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `leboncoinLeboncoinScraperHealthCheckHead()`

```php
leboncoinLeboncoinScraperHealthCheckHead(): mixed
```

Leboncoin scraper health check

Check health of the Leboncoin scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->leboncoinLeboncoinScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinLeboncoinScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `leboncoinListCategories()`

```php
leboncoinListCategories(): mixed
```

List categories

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->leboncoinListCategories();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinListCategories: ', $e->getMessage(), PHP_EOL;
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

## `leboncoinListDepartments()`

```php
leboncoinListDepartments($region_id): mixed
```

List departments

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$region_id = 'region_id_example'; // string

try {
    $result = $apiInstance->leboncoinListDepartments($region_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinListDepartments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **region_id** | **string**|  | [optional] |

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

## `leboncoinListMarkets()`

```php
leboncoinListMarkets(): mixed
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


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->leboncoinListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `leboncoinListRegions()`

```php
leboncoinListRegions(): mixed
```

List regions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->leboncoinListRegions();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinListRegions: ', $e->getMessage(), PHP_EOL;
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

## `leboncoinLocationAutocomplete()`

```php
leboncoinLocationAutocomplete($q): mixed
```

Location autocomplete

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Place name

try {
    $result = $apiInstance->leboncoinLocationAutocomplete($q);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinLocationAutocomplete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Place name | |

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

## `leboncoinSearchLeboncoinAds()`

```php
leboncoinSearchLeboncoinAds($text, $category, $region_id, $department_id, $city, $zipcode, $price_min, $price_max, $owner_type, $ad_type, $sort, $page, $limit): mixed
```

Search Leboncoin ads

Search Leboncoin classifieds (France; scope by region/department/city).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LeboncoinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$text = 'text_example'; // string | Free-text query
$category = 'category_example'; // string | Category id (see /categories)
$region_id = 'region_id_example'; // string | Region id (see /regions)
$department_id = 'department_id_example'; // string | Department id, e.g. 75
$city = 'city_example'; // string
$zipcode = 'zipcode_example'; // string
$price_min = 56; // int
$price_max = 56; // int
$owner_type = 'all'; // string | all | pro | private
$ad_type = 'offer'; // string | offer | demand
$sort = 'relevance'; // string | relevance|newest|oldest|price_low|price_high
$page = 1; // int
$limit = 35; // int

try {
    $result = $apiInstance->leboncoinSearchLeboncoinAds($text, $category, $region_id, $department_id, $city, $zipcode, $price_min, $price_max, $owner_type, $ad_type, $sort, $page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeboncoinApi->leboncoinSearchLeboncoinAds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **text** | **string**| Free-text query | [optional] |
| **category** | **string**| Category id (see /categories) | [optional] |
| **region_id** | **string**| Region id (see /regions) | [optional] |
| **department_id** | **string**| Department id, e.g. 75 | [optional] |
| **city** | **string**|  | [optional] |
| **zipcode** | **string**|  | [optional] |
| **price_min** | **int**|  | [optional] |
| **price_max** | **int**|  | [optional] |
| **owner_type** | **string**| all | pro | private | [optional] [default to &#39;all&#39;] |
| **ad_type** | **string**| offer | demand | [optional] [default to &#39;offer&#39;] |
| **sort** | **string**| relevance|newest|oldest|price_low|price_high | [optional] [default to &#39;relevance&#39;] |
| **page** | **int**|  | [optional] [default to 1] |
| **limit** | **int**|  | [optional] [default to 35] |

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

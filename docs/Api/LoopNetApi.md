# ScrapeBadger\LoopNetApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**loopnetGetBrokerProfile()**](LoopNetApi.md#loopnetGetBrokerProfile) | **GET** /v1/loopnet/brokers/{slug}/{broker_id} | Get broker profile |
| [**loopnetGetListingDetail()**](LoopNetApi.md#loopnetGetListingDetail) | **GET** /v1/loopnet/listings/{listing_id} | Get listing detail |
| [**loopnetListCoverageMarkets()**](LoopNetApi.md#loopnetListCoverageMarkets) | **GET** /v1/loopnet/markets | List coverage markets |
| [**loopnetListPropertyTypes()**](LoopNetApi.md#loopnetListPropertyTypes) | **GET** /v1/loopnet/property-types | List property types |
| [**loopnetLoopnetScraperHealthCheck()**](LoopNetApi.md#loopnetLoopnetScraperHealthCheck) | **GET** /v1/loopnet/health | LoopNet scraper health check |
| [**loopnetLoopnetScraperHealthCheckHead()**](LoopNetApi.md#loopnetLoopnetScraperHealthCheckHead) | **HEAD** /v1/loopnet/health | LoopNet scraper health check |
| [**loopnetSearchCommercialRealEstate()**](LoopNetApi.md#loopnetSearchCommercialRealEstate) | **GET** /v1/loopnet/search | Search commercial real estate |


## `loopnetGetBrokerProfile()`

```php
loopnetGetBrokerProfile($slug, $broker_id, $market): mixed
```

Get broker profile

Get a LoopNet broker profile + their listings by slug + id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LoopNetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = 'slug_example'; // string
$broker_id = 'broker_id_example'; // string
$market = 'us'; // string | us|ca|uk|fr|es

try {
    $result = $apiInstance->loopnetGetBrokerProfile($slug, $broker_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoopNetApi->loopnetGetBrokerProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **slug** | **string**|  | |
| **broker_id** | **string**|  | |
| **market** | **string**| us|ca|uk|fr|es | [optional] [default to &#39;us&#39;] |

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

## `loopnetGetListingDetail()`

```php
loopnetGetListingDetail($listing_id, $market): mixed
```

Get listing detail

Get a single LoopNet listing's full detail by its numeric id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LoopNetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$listing_id = 'listing_id_example'; // string
$market = 'us'; // string | us|ca|uk|fr|es

try {
    $result = $apiInstance->loopnetGetListingDetail($listing_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoopNetApi->loopnetGetListingDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **listing_id** | **string**|  | |
| **market** | **string**| us|ca|uk|fr|es | [optional] [default to &#39;us&#39;] |

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

## `loopnetListCoverageMarkets()`

```php
loopnetListCoverageMarkets(): mixed
```

List coverage markets

List LoopNet coverage markets (US, CA, UK, FR, ES).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LoopNetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->loopnetListCoverageMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoopNetApi->loopnetListCoverageMarkets: ', $e->getMessage(), PHP_EOL;
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

## `loopnetListPropertyTypes()`

```php
loopnetListPropertyTypes(): mixed
```

List property types

List LoopNet property-type facets accepted by /search.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LoopNetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->loopnetListPropertyTypes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoopNetApi->loopnetListPropertyTypes: ', $e->getMessage(), PHP_EOL;
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

## `loopnetLoopnetScraperHealthCheck()`

```php
loopnetLoopnetScraperHealthCheck(): mixed
```

LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LoopNetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->loopnetLoopnetScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoopNetApi->loopnetLoopnetScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `loopnetLoopnetScraperHealthCheckHead()`

```php
loopnetLoopnetScraperHealthCheckHead(): mixed
```

LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LoopNetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->loopnetLoopnetScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoopNetApi->loopnetLoopnetScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `loopnetSearchCommercialRealEstate()`

```php
loopnetSearchCommercialRealEstate($location, $market, $listing_type, $property_type, $page, $min_price, $max_price, $price_type, $min_size, $max_size): mixed
```

Search commercial real estate

Search LoopNet for-lease / for-sale / auction listings across all markets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LoopNetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | City/state, ZIP, state code, or 'usa'
$market = 'us'; // string | us|ca|uk|fr|es
$listing_type = 'for-lease'; // string | for-lease|for-sale|auctions
$property_type = 'property_type_example'; // string | Slug from /property-types
$page = 1; // int
$min_price = 56; // int
$max_price = 56; // int
$price_type = 'price_type_example'; // string | unit | sf | acre
$min_size = 56; // int
$max_size = 56; // int

try {
    $result = $apiInstance->loopnetSearchCommercialRealEstate($location, $market, $listing_type, $property_type, $page, $min_price, $max_price, $price_type, $min_size, $max_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoopNetApi->loopnetSearchCommercialRealEstate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| City/state, ZIP, state code, or &#39;usa&#39; | |
| **market** | **string**| us|ca|uk|fr|es | [optional] [default to &#39;us&#39;] |
| **listing_type** | **string**| for-lease|for-sale|auctions | [optional] [default to &#39;for-lease&#39;] |
| **property_type** | **string**| Slug from /property-types | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **min_price** | **int**|  | [optional] |
| **max_price** | **int**|  | [optional] |
| **price_type** | **string**| unit | sf | acre | [optional] |
| **min_size** | **int**|  | [optional] |
| **max_size** | **int**|  | [optional] |

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

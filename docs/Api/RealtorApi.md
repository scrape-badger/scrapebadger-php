# ScrapeBadger\RealtorApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**realtorGetFullPropertyDetail()**](RealtorApi.md#realtorGetFullPropertyDetail) | **GET** /v1/realtor/properties/{property_id} | Get full property detail |
| [**realtorListMarkets()**](RealtorApi.md#realtorListMarkets) | **GET** /v1/realtor/markets | List markets |
| [**realtorLocationAutocomplete()**](RealtorApi.md#realtorLocationAutocomplete) | **GET** /v1/realtor/autocomplete | Location autocomplete |
| [**realtorRealtorScraperHealthCheck()**](RealtorApi.md#realtorRealtorScraperHealthCheck) | **GET** /v1/realtor/health | Realtor scraper health check |
| [**realtorRealtorScraperHealthCheckHead()**](RealtorApi.md#realtorRealtorScraperHealthCheckHead) | **HEAD** /v1/realtor/health | Realtor scraper health check |
| [**realtorSearchPropertyListings()**](RealtorApi.md#realtorSearchPropertyListings) | **GET** /v1/realtor/search | Search property listings |


## `realtorGetFullPropertyDetail()`

```php
realtorGetFullPropertyDetail($property_id, $market): mixed
```

Get full property detail

Full listing detail: features, tax & price history, schools, photos, agents.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RealtorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$property_id = 'property_id_example'; // string
$market = 'us'; // string | us (realtor.com) | ca (realtor.ca)

try {
    $result = $apiInstance->realtorGetFullPropertyDetail($property_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RealtorApi->realtorGetFullPropertyDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **property_id** | **string**|  | |
| **market** | **string**| us (realtor.com) | ca (realtor.ca) | [optional] [default to &#39;us&#39;] |

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

## `realtorListMarkets()`

```php
realtorListMarkets(): mixed
```

List markets

List supported Realtor markets (US = realtor.com, CA = realtor.ca).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RealtorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->realtorListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RealtorApi->realtorListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `realtorLocationAutocomplete()`

```php
realtorLocationAutocomplete($query, $market, $limit): mixed
```

Location autocomplete

Resolve a location query into candidate places to feed /search.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RealtorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Freetext location (city, ZIP/postal, address…)
$market = 'us'; // string | us (realtor.com) | ca (realtor.ca)
$limit = 10; // int

try {
    $result = $apiInstance->realtorLocationAutocomplete($query, $market, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RealtorApi->realtorLocationAutocomplete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Freetext location (city, ZIP/postal, address…) | |
| **market** | **string**| us (realtor.com) | ca (realtor.ca) | [optional] [default to &#39;us&#39;] |
| **limit** | **int**|  | [optional] [default to 10] |

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

## `realtorRealtorScraperHealthCheck()`

```php
realtorRealtorScraperHealthCheck(): mixed
```

Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RealtorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->realtorRealtorScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RealtorApi->realtorRealtorScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `realtorRealtorScraperHealthCheckHead()`

```php
realtorRealtorScraperHealthCheckHead(): mixed
```

Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RealtorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->realtorRealtorScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RealtorApi->realtorRealtorScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `realtorSearchPropertyListings()`

```php
realtorSearchPropertyListings($location, $market, $status, $price_min, $price_max, $beds_min, $baths_min, $sqft_min, $sqft_max, $property_type, $sort, $page, $limit, $lat_min, $lat_max, $lng_min, $lng_max): mixed
```

Search property listings

Search for-sale/for-rent/sold listings with rich filters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RealtorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | 'Austin, TX', a ZIP, 'Toronto, ON'…
$market = 'us'; // string | us (realtor.com) | ca (realtor.ca)
$status = 'for_sale'; // string | for_sale | for_rent | sold | pending
$price_min = 3.4; // float
$price_max = 3.4; // float
$beds_min = 56; // int
$baths_min = 56; // int
$sqft_min = 56; // int | US only
$sqft_max = 56; // int | US only
$property_type = 'property_type_example'; // string | US only, CSV of property types
$sort = 'relevant'; // string | relevant | newest | price_low | price_high | photo_count
$page = 1; // int
$limit = 56; // int
$lat_min = 3.4; // float | CA bbox south
$lat_max = 3.4; // float | CA bbox north
$lng_min = 3.4; // float | CA bbox west
$lng_max = 3.4; // float | CA bbox east

try {
    $result = $apiInstance->realtorSearchPropertyListings($location, $market, $status, $price_min, $price_max, $beds_min, $baths_min, $sqft_min, $sqft_max, $property_type, $sort, $page, $limit, $lat_min, $lat_max, $lng_min, $lng_max);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RealtorApi->realtorSearchPropertyListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| &#39;Austin, TX&#39;, a ZIP, &#39;Toronto, ON&#39;… | [optional] |
| **market** | **string**| us (realtor.com) | ca (realtor.ca) | [optional] [default to &#39;us&#39;] |
| **status** | **string**| for_sale | for_rent | sold | pending | [optional] [default to &#39;for_sale&#39;] |
| **price_min** | **float**|  | [optional] |
| **price_max** | **float**|  | [optional] |
| **beds_min** | **int**|  | [optional] |
| **baths_min** | **int**|  | [optional] |
| **sqft_min** | **int**| US only | [optional] |
| **sqft_max** | **int**| US only | [optional] |
| **property_type** | **string**| US only, CSV of property types | [optional] |
| **sort** | **string**| relevant | newest | price_low | price_high | photo_count | [optional] [default to &#39;relevant&#39;] |
| **page** | **int**|  | [optional] [default to 1] |
| **limit** | **int**|  | [optional] |
| **lat_min** | **float**| CA bbox south | [optional] |
| **lat_max** | **float**| CA bbox north | [optional] |
| **lng_min** | **float**| CA bbox west | [optional] |
| **lng_max** | **float**| CA bbox east | [optional] |

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

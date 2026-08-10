# ScrapeBadger\ApartmentsApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apartmentsApartmentsScraperHealthCheck()**](ApartmentsApi.md#apartmentsApartmentsScraperHealthCheck) | **GET** /v1/apartments/health | Apartments scraper health check |
| [**apartmentsApartmentsScraperHealthCheckHead()**](ApartmentsApi.md#apartmentsApartmentsScraperHealthCheckHead) | **HEAD** /v1/apartments/health | Apartments scraper health check |
| [**apartmentsGetPropertyDetailBySlugId()**](ApartmentsApi.md#apartmentsGetPropertyDetailBySlugId) | **GET** /v1/apartments/properties/{slug}/{property_id} | Get property detail by slug + id |
| [**apartmentsGetPropertyDetailByUrl()**](ApartmentsApi.md#apartmentsGetPropertyDetailByUrl) | **GET** /v1/apartments/property | Get property detail by URL |
| [**apartmentsSearchRentalListings()**](ApartmentsApi.md#apartmentsSearchRentalListings) | **GET** /v1/apartments/search | Search rental listings |


## `apartmentsApartmentsScraperHealthCheck()`

```php
apartmentsApartmentsScraperHealthCheck(): mixed
```

Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ApartmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apartmentsApartmentsScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApartmentsApi->apartmentsApartmentsScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `apartmentsApartmentsScraperHealthCheckHead()`

```php
apartmentsApartmentsScraperHealthCheckHead(): mixed
```

Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ApartmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apartmentsApartmentsScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApartmentsApi->apartmentsApartmentsScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `apartmentsGetPropertyDetailBySlugId()`

```php
apartmentsGetPropertyDetailBySlugId($slug, $property_id): mixed
```

Get property detail by slug + id

Get a property by its SEO slug and 7-character listing id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ApartmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = 'slug_example'; // string
$property_id = 'property_id_example'; // string

try {
    $result = $apiInstance->apartmentsGetPropertyDetailBySlugId($slug, $property_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApartmentsApi->apartmentsGetPropertyDetailBySlugId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **slug** | **string**|  | |
| **property_id** | **string**|  | |

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

## `apartmentsGetPropertyDetailByUrl()`

```php
apartmentsGetPropertyDetailByUrl($url): mixed
```

Get property detail by URL

Get an apartments.com property with full per-unit pricing and availability.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ApartmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$url = 'url_example'; // string | Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/

try {
    $result = $apiInstance->apartmentsGetPropertyDetailByUrl($url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApartmentsApi->apartmentsGetPropertyDetailByUrl: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **url** | **string**| Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/ | |

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

## `apartmentsSearchRentalListings()`

```php
apartmentsSearchRentalListings($location, $page, $beds, $min_price, $max_price): mixed
```

Search rental listings

Search apartments.com for rental properties. 40 cards per page.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ApartmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | apartments.com location slug, e.g. 'kansas-city-mo'
$page = 1; // int
$beds = 56; // int | 0=studio, 1-4 bedrooms
$min_price = 56; // int
$max_price = 56; // int

try {
    $result = $apiInstance->apartmentsSearchRentalListings($location, $page, $beds, $min_price, $max_price);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApartmentsApi->apartmentsSearchRentalListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| apartments.com location slug, e.g. &#39;kansas-city-mo&#39; | |
| **page** | **int**|  | [optional] [default to 1] |
| **beds** | **int**| 0&#x3D;studio, 1-4 bedrooms | [optional] |
| **min_price** | **int**|  | [optional] |
| **max_price** | **int**|  | [optional] |

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

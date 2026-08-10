# ScrapeBadger\IdealistaApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**idealistaAgencyByPhone()**](IdealistaApi.md#idealistaAgencyByPhone) | **GET** /v1/idealista/agency/by-phone/{phone} | Agency by phone |
| [**idealistaAgencyProfileListings()**](IdealistaApi.md#idealistaAgencyProfileListings) | **GET** /v1/idealista/agency/{short_name} | Agency profile + listings |
| [**idealistaGetListingEngagementStats()**](IdealistaApi.md#idealistaGetListingEngagementStats) | **GET** /v1/idealista/properties/{property_code}/stats | Get listing engagement stats |
| [**idealistaGetPropertyDetail()**](IdealistaApi.md#idealistaGetPropertyDetail) | **GET** /v1/idealista/properties/{property_code} | Get property detail |
| [**idealistaIdealistaScraperHealthCheck()**](IdealistaApi.md#idealistaIdealistaScraperHealthCheck) | **GET** /v1/idealista/health | Idealista scraper health check |
| [**idealistaIdealistaScraperHealthCheckHead()**](IdealistaApi.md#idealistaIdealistaScraperHealthCheckHead) | **HEAD** /v1/idealista/health | Idealista scraper health check |
| [**idealistaListMarkets()**](IdealistaApi.md#idealistaListMarkets) | **GET** /v1/idealista/markets | List markets |
| [**idealistaResolveLocations()**](IdealistaApi.md#idealistaResolveLocations) | **GET** /v1/idealista/suggest | Resolve locations |
| [**idealistaSearchAllBeatsResultCap()**](IdealistaApi.md#idealistaSearchAllBeatsResultCap) | **GET** /v1/idealista/search/all | Search all (beats result cap) |
| [**idealistaSearchListings()**](IdealistaApi.md#idealistaSearchListings) | **GET** /v1/idealista/search | Search listings |


## `idealistaAgencyByPhone()`

```php
idealistaAgencyByPhone($phone, $market, $operation, $property_type, $page, $max_items, $include_listings): mixed
```

Agency by phone

Reverse-lookup the agency behind a contact phone (national number), with its listings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\IdealistaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$phone = 'phone_example'; // string
$market = 'es'; // string | es|it|pt
$operation = 'operation_example'; // string | sale|rent
$property_type = 'property_type_example'; // string | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
$page = 1; // int
$max_items = 30; // int
$include_listings = true; // bool

try {
    $result = $apiInstance->idealistaAgencyByPhone($phone, $market, $operation, $property_type, $page, $max_items, $include_listings);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdealistaApi->idealistaAgencyByPhone: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **phone** | **string**|  | |
| **market** | **string**| es|it|pt | [optional] [default to &#39;es&#39;] |
| **operation** | **string**| sale|rent | [optional] |
| **property_type** | **string**| homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **max_items** | **int**|  | [optional] [default to 30] |
| **include_listings** | **bool**|  | [optional] [default to true] |

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

## `idealistaAgencyProfileListings()`

```php
idealistaAgencyProfileListings($short_name, $market, $operation, $property_type, $page, $max_items, $include_listings): mixed
```

Agency profile + listings

An agency's microsite profile plus a page of its listings (by URL-slug shortName).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\IdealistaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$short_name = 'short_name_example'; // string
$market = 'es'; // string | es|it|pt
$operation = 'operation_example'; // string | sale|rent
$property_type = 'property_type_example'; // string | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
$page = 1; // int
$max_items = 30; // int
$include_listings = true; // bool

try {
    $result = $apiInstance->idealistaAgencyProfileListings($short_name, $market, $operation, $property_type, $page, $max_items, $include_listings);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdealistaApi->idealistaAgencyProfileListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **short_name** | **string**|  | |
| **market** | **string**| es|it|pt | [optional] [default to &#39;es&#39;] |
| **operation** | **string**| sale|rent | [optional] |
| **property_type** | **string**| homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **max_items** | **int**|  | [optional] [default to 30] |
| **include_listings** | **bool**|  | [optional] [default to true] |

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

## `idealistaGetListingEngagementStats()`

```php
idealistaGetListingEngagementStats($property_code, $market, $locale): mixed
```

Get listing engagement stats

Engagement counters for a listing: views, email contacts, sent-to-friend, favourites.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\IdealistaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$property_code = 'property_code_example'; // string
$market = 'es'; // string | es|it|pt
$locale = 'en'; // string | Language for stat labels

try {
    $result = $apiInstance->idealistaGetListingEngagementStats($property_code, $market, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdealistaApi->idealistaGetListingEngagementStats: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **property_code** | **string**|  | |
| **market** | **string**| es|it|pt | [optional] [default to &#39;es&#39;] |
| **locale** | **string**| Language for stat labels | [optional] [default to &#39;en&#39;] |

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

## `idealistaGetPropertyDetail()`

```php
idealistaGetPropertyDetail($property_code, $market, $locale): mixed
```

Get property detail

Get a single Idealista listing's full detail (energy cert, characteristics, media).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\IdealistaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$property_code = 'property_code_example'; // string
$market = 'es'; // string | es|it|pt
$locale = 'en'; // string | Response language (en, es, it, pt)

try {
    $result = $apiInstance->idealistaGetPropertyDetail($property_code, $market, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdealistaApi->idealistaGetPropertyDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **property_code** | **string**|  | |
| **market** | **string**| es|it|pt | [optional] [default to &#39;es&#39;] |
| **locale** | **string**| Response language (en, es, it, pt) | [optional] [default to &#39;en&#39;] |

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

## `idealistaIdealistaScraperHealthCheck()`

```php
idealistaIdealistaScraperHealthCheck(): mixed
```

Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\IdealistaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->idealistaIdealistaScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdealistaApi->idealistaIdealistaScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `idealistaIdealistaScraperHealthCheckHead()`

```php
idealistaIdealistaScraperHealthCheckHead(): mixed
```

Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\IdealistaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->idealistaIdealistaScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdealistaApi->idealistaIdealistaScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `idealistaListMarkets()`

```php
idealistaListMarkets(): mixed
```

List markets

List supported Idealista markets (ES, IT, PT).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\IdealistaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->idealistaListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdealistaApi->idealistaListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `idealistaResolveLocations()`

```php
idealistaResolveLocations($query, $operation, $property_type, $market, $locale): mixed
```

Resolve locations

Resolve a free-text query into Idealista location codes for a search.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\IdealistaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Free-text location, e.g. 'sagrada familia'
$operation = 'sale'; // string | sale|rent
$property_type = 'homes'; // string | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
$market = 'es'; // string | es|it|pt
$locale = 'locale_example'; // string | Response language (en, es, it, pt)

try {
    $result = $apiInstance->idealistaResolveLocations($query, $operation, $property_type, $market, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdealistaApi->idealistaResolveLocations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Free-text location, e.g. &#39;sagrada familia&#39; | |
| **operation** | **string**| sale|rent | [optional] [default to &#39;sale&#39;] |
| **property_type** | **string**| homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to &#39;homes&#39;] |
| **market** | **string**| es|it|pt | [optional] [default to &#39;es&#39;] |
| **locale** | **string**| Response language (en, es, it, pt) | [optional] |

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

## `idealistaSearchAllBeatsResultCap()`

```php
idealistaSearchAllBeatsResultCap($location, $operation, $property_type, $market, $max_results, $min_price, $max_price, $min_size, $max_size, $min_rooms, $max_rooms, $locale): mixed
```

Search all (beats result cap)

Full inventory for a location, beating Idealista's ~1800 per-search cap via price-range tiling (deduped). Billed per page fetched.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\IdealistaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | Idealista location code (from /suggest)
$operation = 'sale'; // string | sale|rent
$property_type = 'homes'; // string | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
$market = 'es'; // string | es|it|pt
$max_results = 500; // int
$min_price = 3.4; // float
$max_price = 3.4; // float
$min_size = 3.4; // float
$max_size = 3.4; // float
$min_rooms = 56; // int
$max_rooms = 56; // int
$locale = 'locale_example'; // string | Response language (en, es, it, pt)

try {
    $result = $apiInstance->idealistaSearchAllBeatsResultCap($location, $operation, $property_type, $market, $max_results, $min_price, $max_price, $min_size, $max_size, $min_rooms, $max_rooms, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdealistaApi->idealistaSearchAllBeatsResultCap: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| Idealista location code (from /suggest) | |
| **operation** | **string**| sale|rent | [optional] [default to &#39;sale&#39;] |
| **property_type** | **string**| homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to &#39;homes&#39;] |
| **market** | **string**| es|it|pt | [optional] [default to &#39;es&#39;] |
| **max_results** | **int**|  | [optional] [default to 500] |
| **min_price** | **float**|  | [optional] |
| **max_price** | **float**|  | [optional] |
| **min_size** | **float**|  | [optional] |
| **max_size** | **float**|  | [optional] |
| **min_rooms** | **int**|  | [optional] |
| **max_rooms** | **int**|  | [optional] |
| **locale** | **string**| Response language (en, es, it, pt) | [optional] |

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

## `idealistaSearchListings()`

```php
idealistaSearchListings($location, $operation, $property_type, $market, $page, $max_items, $sort_by, $sort_order, $min_price, $max_price, $min_size, $max_size, $min_rooms, $max_rooms, $locale): mixed
```

Search listings

Search Idealista real-estate listings by location code.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\IdealistaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | Idealista location code (from /suggest)
$operation = 'sale'; // string | sale|rent
$property_type = 'homes'; // string | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
$market = 'es'; // string | es|it|pt
$page = 1; // int
$max_items = 30; // int
$sort_by = 'sort_by_example'; // string | distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds
$sort_order = 'desc'; // string | asc|desc
$min_price = 3.4; // float
$max_price = 3.4; // float
$min_size = 3.4; // float
$max_size = 3.4; // float
$min_rooms = 56; // int
$max_rooms = 56; // int
$locale = 'locale_example'; // string | Response language (en, es, it, pt)

try {
    $result = $apiInstance->idealistaSearchListings($location, $operation, $property_type, $market, $page, $max_items, $sort_by, $sort_order, $min_price, $max_price, $min_size, $max_size, $min_rooms, $max_rooms, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdealistaApi->idealistaSearchListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| Idealista location code (from /suggest) | |
| **operation** | **string**| sale|rent | [optional] [default to &#39;sale&#39;] |
| **property_type** | **string**| homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to &#39;homes&#39;] |
| **market** | **string**| es|it|pt | [optional] [default to &#39;es&#39;] |
| **page** | **int**|  | [optional] [default to 1] |
| **max_items** | **int**|  | [optional] [default to 30] |
| **sort_by** | **string**| distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds | [optional] |
| **sort_order** | **string**| asc|desc | [optional] [default to &#39;desc&#39;] |
| **min_price** | **float**|  | [optional] |
| **max_price** | **float**|  | [optional] |
| **min_size** | **float**|  | [optional] |
| **max_size** | **float**|  | [optional] |
| **min_rooms** | **int**|  | [optional] |
| **max_rooms** | **int**|  | [optional] |
| **locale** | **string**| Response language (en, es, it, pt) | [optional] |

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

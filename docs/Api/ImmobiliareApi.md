# ScrapeBadger\ImmobiliareApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**immobiliareGetAgencyProfile()**](ImmobiliareApi.md#immobiliareGetAgencyProfile) | **GET** /v1/immobiliare/agencies/{agency_id} | Get agency profile |
| [**immobiliareGetAnAgencySListings()**](ImmobiliareApi.md#immobiliareGetAnAgencySListings) | **GET** /v1/immobiliare/agencies/{agency_id}/listings | Get an agency&#39;s listings |
| [**immobiliareGetListingDetail()**](ImmobiliareApi.md#immobiliareGetListingDetail) | **GET** /v1/immobiliare/listings/{listing_id} | Get listing detail |
| [**immobiliareImmobiliareScraperHealthCheck()**](ImmobiliareApi.md#immobiliareImmobiliareScraperHealthCheck) | **GET** /v1/immobiliare/health | Immobiliare scraper health check |
| [**immobiliareImmobiliareScraperHealthCheckHead()**](ImmobiliareApi.md#immobiliareImmobiliareScraperHealthCheckHead) | **HEAD** /v1/immobiliare/health | Immobiliare scraper health check |
| [**immobiliareListFilterEnums()**](ImmobiliareApi.md#immobiliareListFilterEnums) | **GET** /v1/immobiliare/reference | List filter enums |
| [**immobiliareListMarkets()**](ImmobiliareApi.md#immobiliareListMarkets) | **GET** /v1/immobiliare/markets | List markets |
| [**immobiliareLocationAutocomplete()**](ImmobiliareApi.md#immobiliareLocationAutocomplete) | **GET** /v1/immobiliare/autocomplete | Location autocomplete |
| [**immobiliarePriceMTimeSeries()**](ImmobiliareApi.md#immobiliarePriceMTimeSeries) | **GET** /v1/immobiliare/market-insights/prices | Price €/m² time series |
| [**immobiliareSearchListings()**](ImmobiliareApi.md#immobiliareSearchListings) | **GET** /v1/immobiliare/search | Search listings |


## `immobiliareGetAgencyProfile()`

```php
immobiliareGetAgencyProfile($agency_id, $market): mixed
```

Get agency profile

Public agency/advertiser profile.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ImmobiliareApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$agency_id = 56; // int
$market = 'it'; // string | it | es | gr | lu

try {
    $result = $apiInstance->immobiliareGetAgencyProfile($agency_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImmobiliareApi->immobiliareGetAgencyProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **agency_id** | **int**|  | |
| **market** | **string**| it | es | gr | lu | [optional] [default to &#39;it&#39;] |

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

## `immobiliareGetAnAgencySListings()`

```php
immobiliareGetAnAgencySListings($agency_id, $market, $contract, $page): mixed
```

Get an agency's listings

An agency's active listings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ImmobiliareApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$agency_id = 56; // int
$market = 'it'; // string | it | es | gr | lu
$contract = 'sale'; // string | sale | rent
$page = 1; // int

try {
    $result = $apiInstance->immobiliareGetAnAgencySListings($agency_id, $market, $contract, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImmobiliareApi->immobiliareGetAnAgencySListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **agency_id** | **int**|  | |
| **market** | **string**| it | es | gr | lu | [optional] [default to &#39;it&#39;] |
| **contract** | **string**| sale | rent | [optional] [default to &#39;sale&#39;] |
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

## `immobiliareGetListingDetail()`

```php
immobiliareGetListingDetail($listing_id, $market): mixed
```

Get listing detail

Full detail for a single listing.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ImmobiliareApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$listing_id = 56; // int
$market = 'it'; // string | it | es | gr | lu

try {
    $result = $apiInstance->immobiliareGetListingDetail($listing_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImmobiliareApi->immobiliareGetListingDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **listing_id** | **int**|  | |
| **market** | **string**| it | es | gr | lu | [optional] [default to &#39;it&#39;] |

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

## `immobiliareImmobiliareScraperHealthCheck()`

```php
immobiliareImmobiliareScraperHealthCheck(): mixed
```

Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ImmobiliareApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->immobiliareImmobiliareScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImmobiliareApi->immobiliareImmobiliareScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `immobiliareImmobiliareScraperHealthCheckHead()`

```php
immobiliareImmobiliareScraperHealthCheckHead(): mixed
```

Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ImmobiliareApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->immobiliareImmobiliareScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImmobiliareApi->immobiliareImmobiliareScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `immobiliareListFilterEnums()`

```php
immobiliareListFilterEnums(): mixed
```

List filter enums

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ImmobiliareApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->immobiliareListFilterEnums();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImmobiliareApi->immobiliareListFilterEnums: ', $e->getMessage(), PHP_EOL;
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

## `immobiliareListMarkets()`

```php
immobiliareListMarkets(): mixed
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


$apiInstance = new ScrapeBadger\Api\ImmobiliareApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->immobiliareListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImmobiliareApi->immobiliareListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `immobiliareLocationAutocomplete()`

```php
immobiliareLocationAutocomplete($query, $market): mixed
```

Location autocomplete

Resolve a place name to region/province/city ids usable in search.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ImmobiliareApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Free-text place name, e.g. 'Milano'
$market = 'it'; // string | it | es | gr | lu

try {
    $result = $apiInstance->immobiliareLocationAutocomplete($query, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImmobiliareApi->immobiliareLocationAutocomplete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Free-text place name, e.g. &#39;Milano&#39; | |
| **market** | **string**| it | es | gr | lu | [optional] [default to &#39;it&#39;] |

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

## `immobiliarePriceMTimeSeries()`

```php
immobiliarePriceMTimeSeries($region_id, $market, $province_id, $city_id, $contract): mixed
```

Price €/m² time series

Historical €/m² price statistics for an area.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ImmobiliareApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$region_id = 'region_id_example'; // string | Region id, e.g. 'lom'
$market = 'it'; // string | it | es | gr | lu
$province_id = 'province_id_example'; // string | Province id, e.g. 'MI'
$city_id = 'city_id_example'; // string | City id (idComune)
$contract = 'sale'; // string | sale | rent

try {
    $result = $apiInstance->immobiliarePriceMTimeSeries($region_id, $market, $province_id, $city_id, $contract);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImmobiliareApi->immobiliarePriceMTimeSeries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **region_id** | **string**| Region id, e.g. &#39;lom&#39; | |
| **market** | **string**| it | es | gr | lu | [optional] [default to &#39;it&#39;] |
| **province_id** | **string**| Province id, e.g. &#39;MI&#39; | [optional] |
| **city_id** | **string**| City id (idComune) | [optional] |
| **contract** | **string**| sale | rent | [optional] [default to &#39;sale&#39;] |

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

## `immobiliareSearchListings()`

```php
immobiliareSearchListings($market, $location, $region_id, $province_id, $city_id, $contract, $category, $price_min, $price_max, $surface_min, $surface_max, $rooms_min, $rooms_max, $bathrooms_min, $sort, $page): mixed
```

Search listings

Search Immobiliare-group listings (scope by location + contract + filters).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ImmobiliareApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$market = 'it'; // string | it | es | gr | lu
$location = 'location_example'; // string | Free-text place (auto-resolved)
$region_id = 'region_id_example'; // string | fkRegione (from /autocomplete)
$province_id = 'province_id_example'; // string | idProvincia (from /autocomplete)
$city_id = 'city_id_example'; // string | idComune (from /autocomplete)
$contract = 'sale'; // string | sale | rent
$category = 'residential'; // string | see /reference
$price_min = 56; // int
$price_max = 56; // int
$surface_min = 56; // int
$surface_max = 56; // int
$rooms_min = 56; // int
$rooms_max = 56; // int
$bathrooms_min = 56; // int
$sort = 'relevance'; // string | see /reference
$page = 1; // int

try {
    $result = $apiInstance->immobiliareSearchListings($market, $location, $region_id, $province_id, $city_id, $contract, $category, $price_min, $price_max, $surface_min, $surface_max, $rooms_min, $rooms_max, $bathrooms_min, $sort, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImmobiliareApi->immobiliareSearchListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **market** | **string**| it | es | gr | lu | [optional] [default to &#39;it&#39;] |
| **location** | **string**| Free-text place (auto-resolved) | [optional] |
| **region_id** | **string**| fkRegione (from /autocomplete) | [optional] |
| **province_id** | **string**| idProvincia (from /autocomplete) | [optional] |
| **city_id** | **string**| idComune (from /autocomplete) | [optional] |
| **contract** | **string**| sale | rent | [optional] [default to &#39;sale&#39;] |
| **category** | **string**| see /reference | [optional] [default to &#39;residential&#39;] |
| **price_min** | **int**|  | [optional] |
| **price_max** | **int**|  | [optional] |
| **surface_min** | **int**|  | [optional] |
| **surface_max** | **int**|  | [optional] |
| **rooms_min** | **int**|  | [optional] |
| **rooms_max** | **int**|  | [optional] |
| **bathrooms_min** | **int**|  | [optional] |
| **sort** | **string**| see /reference | [optional] [default to &#39;relevance&#39;] |
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

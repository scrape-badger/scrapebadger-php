# ScrapeBadger\ZillowApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**zillowGetAgentProfileListings()**](ZillowApi.md#zillowGetAgentProfileListings) | **GET** /v1/zillow/agent | Get agent profile + listings |
| [**zillowGetPropertyDetail()**](ZillowApi.md#zillowGetPropertyDetail) | **GET** /v1/zillow/property/{zpid} | Get property detail |
| [**zillowGetPropertyDetailByUrl()**](ZillowApi.md#zillowGetPropertyDetailByUrl) | **GET** /v1/zillow/property | Get property detail by URL |
| [**zillowListCoverageMarkets()**](ZillowApi.md#zillowListCoverageMarkets) | **GET** /v1/zillow/markets | List coverage markets |
| [**zillowRegionAddressSuggestions()**](ZillowApi.md#zillowRegionAddressSuggestions) | **GET** /v1/zillow/autocomplete | Region/address suggestions |
| [**zillowSearchProperties()**](ZillowApi.md#zillowSearchProperties) | **GET** /v1/zillow/search | Search properties |
| [**zillowZillowScraperHealthCheck()**](ZillowApi.md#zillowZillowScraperHealthCheck) | **GET** /v1/zillow/health | Zillow scraper health check |
| [**zillowZillowScraperHealthCheckHead()**](ZillowApi.md#zillowZillowScraperHealthCheckHead) | **HEAD** /v1/zillow/health | Zillow scraper health check |


## `zillowGetAgentProfileListings()`

```php
zillowGetAgentProfileListings($username, $url): mixed
```

Get agent profile + listings

Get a Zillow professional's profile and their active listings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ZillowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Zillow profile username
$url = 'url_example'; // string | Full Zillow /profile/... URL

try {
    $result = $apiInstance->zillowGetAgentProfileListings($username, $url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ZillowApi->zillowGetAgentProfileListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Zillow profile username | [optional] |
| **url** | **string**| Full Zillow /profile/... URL | [optional] |

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

## `zillowGetPropertyDetail()`

```php
zillowGetPropertyDetail($zpid): mixed
```

Get property detail

Get a single Zillow property's full detail by zpid.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ZillowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$zpid = 'zpid_example'; // string

try {
    $result = $apiInstance->zillowGetPropertyDetail($zpid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ZillowApi->zillowGetPropertyDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **zpid** | **string**|  | |

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

## `zillowGetPropertyDetailByUrl()`

```php
zillowGetPropertyDetailByUrl($url): mixed
```

Get property detail by URL

Get a single Zillow property's full detail by its homedetails URL.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ZillowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$url = 'url_example'; // string | Full Zillow /homedetails/... URL

try {
    $result = $apiInstance->zillowGetPropertyDetailByUrl($url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ZillowApi->zillowGetPropertyDetailByUrl: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **url** | **string**| Full Zillow /homedetails/... URL | |

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

## `zillowListCoverageMarkets()`

```php
zillowListCoverageMarkets(): mixed
```

List coverage markets

List Zillow coverage regions (US + Canada).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ZillowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->zillowListCoverageMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ZillowApi->zillowListCoverageMarkets: ', $e->getMessage(), PHP_EOL;
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

## `zillowRegionAddressSuggestions()`

```php
zillowRegionAddressSuggestions($query): mixed
```

Region/address suggestions

Resolve a search term to Zillow regions/addresses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ZillowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial location — city, ZIP, address, neighborhood

try {
    $result = $apiInstance->zillowRegionAddressSuggestions($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ZillowApi->zillowRegionAddressSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial location — city, ZIP, address, neighborhood | |

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

## `zillowSearchProperties()`

```php
zillowSearchProperties($location, $status, $page, $sort, $price_min, $price_max, $beds_min, $baths_min, $home_type, $sqft_min, $sqft_max, $lot_min, $lot_max, $year_built_min, $year_built_max, $hoa_max, $keywords, $days_on, $north, $south, $east, $west): mixed
```

Search properties

Search Zillow for for-sale / for-rent / recently-sold properties.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ZillowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | City/state, ZIP, address or neighborhood
$status = 'for_sale'; // string | for_sale|for_rent|sold
$page = 1; // int
$sort = 'sort_example'; // string | homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built
$price_min = 56; // int
$price_max = 56; // int
$beds_min = 56; // int
$baths_min = 3.4; // float
$home_type = 'home_type_example'; // string | houses|condos|townhomes|apartments|manufactured|lots|multi_family
$sqft_min = 56; // int
$sqft_max = 56; // int
$lot_min = 56; // int
$lot_max = 56; // int
$year_built_min = 56; // int
$year_built_max = 56; // int
$hoa_max = 56; // int
$keywords = 'keywords_example'; // string
$days_on = 'days_on_example'; // string
$north = 3.4; // float | Map bounds for tiling past the 820 cap
$south = 3.4; // float
$east = 3.4; // float
$west = 3.4; // float

try {
    $result = $apiInstance->zillowSearchProperties($location, $status, $page, $sort, $price_min, $price_max, $beds_min, $baths_min, $home_type, $sqft_min, $sqft_max, $lot_min, $lot_max, $year_built_min, $year_built_max, $hoa_max, $keywords, $days_on, $north, $south, $east, $west);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ZillowApi->zillowSearchProperties: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| City/state, ZIP, address or neighborhood | |
| **status** | **string**| for_sale|for_rent|sold | [optional] [default to &#39;for_sale&#39;] |
| **page** | **int**|  | [optional] [default to 1] |
| **sort** | **string**| homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built | [optional] |
| **price_min** | **int**|  | [optional] |
| **price_max** | **int**|  | [optional] |
| **beds_min** | **int**|  | [optional] |
| **baths_min** | **float**|  | [optional] |
| **home_type** | **string**| houses|condos|townhomes|apartments|manufactured|lots|multi_family | [optional] |
| **sqft_min** | **int**|  | [optional] |
| **sqft_max** | **int**|  | [optional] |
| **lot_min** | **int**|  | [optional] |
| **lot_max** | **int**|  | [optional] |
| **year_built_min** | **int**|  | [optional] |
| **year_built_max** | **int**|  | [optional] |
| **hoa_max** | **int**|  | [optional] |
| **keywords** | **string**|  | [optional] |
| **days_on** | **string**|  | [optional] |
| **north** | **float**| Map bounds for tiling past the 820 cap | [optional] |
| **south** | **float**|  | [optional] |
| **east** | **float**|  | [optional] |
| **west** | **float**|  | [optional] |

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

## `zillowZillowScraperHealthCheck()`

```php
zillowZillowScraperHealthCheck(): mixed
```

Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ZillowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->zillowZillowScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ZillowApi->zillowZillowScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `zillowZillowScraperHealthCheckHead()`

```php
zillowZillowScraperHealthCheckHead(): mixed
```

Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ZillowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->zillowZillowScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ZillowApi->zillowZillowScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

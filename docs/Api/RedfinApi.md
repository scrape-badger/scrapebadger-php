# ScrapeBadger\RedfinApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**redfinGetAgentProfileListings()**](RedfinApi.md#redfinGetAgentProfileListings) | **GET** /v1/redfin/agent | Get agent profile + listings |
| [**redfinGetPropertyDetail()**](RedfinApi.md#redfinGetPropertyDetail) | **GET** /v1/redfin/property/{property_id} | Get property detail |
| [**redfinGetPropertyDetailByUrl()**](RedfinApi.md#redfinGetPropertyDetailByUrl) | **GET** /v1/redfin/property | Get property detail by URL |
| [**redfinListCoverageMarkets()**](RedfinApi.md#redfinListCoverageMarkets) | **GET** /v1/redfin/markets | List coverage markets |
| [**redfinRedfinScraperHealthCheck()**](RedfinApi.md#redfinRedfinScraperHealthCheck) | **GET** /v1/redfin/health | Redfin scraper health check |
| [**redfinRedfinScraperHealthCheckHead()**](RedfinApi.md#redfinRedfinScraperHealthCheckHead) | **HEAD** /v1/redfin/health | Redfin scraper health check |
| [**redfinRegionAddressSuggestions()**](RedfinApi.md#redfinRegionAddressSuggestions) | **GET** /v1/redfin/autocomplete | Region/address suggestions |
| [**redfinSearchProperties()**](RedfinApi.md#redfinSearchProperties) | **GET** /v1/redfin/search | Search properties |


## `redfinGetAgentProfileListings()`

```php
redfinGetAgentProfileListings($url, $agent_id): mixed
```

Get agent profile + listings

Get a Redfin real-estate agent's profile and their active listings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedfinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$url = 'url_example'; // string | Full Redfin /realestateagents/ URL
$agent_id = 'agent_id_example'; // string | Redfin agent id

try {
    $result = $apiInstance->redfinGetAgentProfileListings($url, $agent_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedfinApi->redfinGetAgentProfileListings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **url** | **string**| Full Redfin /realestateagents/ URL | [optional] |
| **agent_id** | **string**| Redfin agent id | [optional] |

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

## `redfinGetPropertyDetail()`

```php
redfinGetPropertyDetail($property_id): mixed
```

Get property detail

Get a single Redfin property's full detail by its numeric propertyId.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedfinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$property_id = 'property_id_example'; // string

try {
    $result = $apiInstance->redfinGetPropertyDetail($property_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedfinApi->redfinGetPropertyDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `redfinGetPropertyDetailByUrl()`

```php
redfinGetPropertyDetailByUrl($url): mixed
```

Get property detail by URL

Get a single Redfin property's full detail by its home URL.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedfinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$url = 'url_example'; // string | Full Redfin property URL (/CA/City/.../home/12345678)

try {
    $result = $apiInstance->redfinGetPropertyDetailByUrl($url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedfinApi->redfinGetPropertyDetailByUrl: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **url** | **string**| Full Redfin property URL (/CA/City/.../home/12345678) | |

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

## `redfinListCoverageMarkets()`

```php
redfinListCoverageMarkets(): mixed
```

List coverage markets

List Redfin coverage regions (US).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedfinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->redfinListCoverageMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedfinApi->redfinListCoverageMarkets: ', $e->getMessage(), PHP_EOL;
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

## `redfinRedfinScraperHealthCheck()`

```php
redfinRedfinScraperHealthCheck(): mixed
```

Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedfinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->redfinRedfinScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedfinApi->redfinRedfinScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `redfinRedfinScraperHealthCheckHead()`

```php
redfinRedfinScraperHealthCheckHead(): mixed
```

Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedfinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->redfinRedfinScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedfinApi->redfinRedfinScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `redfinRegionAddressSuggestions()`

```php
redfinRegionAddressSuggestions($query): mixed
```

Region/address suggestions

Resolve a search term to Redfin regions/addresses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedfinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial location — city, ZIP, address, neighborhood

try {
    $result = $apiInstance->redfinRegionAddressSuggestions($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedfinApi->redfinRegionAddressSuggestions: ', $e->getMessage(), PHP_EOL;
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

## `redfinSearchProperties()`

```php
redfinSearchProperties($location, $page, $sort, $price_min, $price_max, $beds_min, $baths_min, $home_type, $sqft_min, $sqft_max, $lot_min, $lot_max, $year_built_min, $year_built_max, $max_days_on_market, $north, $south, $east, $west): mixed
```

Search properties

Search Redfin for for-sale / for-rent / recently-sold properties.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RedfinApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | City/state, ZIP, address or neighborhood
$page = 1; // int
$sort = 'sort_example'; // string | relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths
$price_min = 56; // int
$price_max = 56; // int
$beds_min = 56; // int
$baths_min = 3.4; // float
$home_type = 'home_type_example'; // string | house|condo|townhouse|multi_family|land|mobile|coop|other
$sqft_min = 56; // int
$sqft_max = 56; // int
$lot_min = 56; // int
$lot_max = 56; // int
$year_built_min = 56; // int
$year_built_max = 56; // int
$max_days_on_market = 56; // int
$north = 3.4; // float | Map bounds for tiling past the cap
$south = 3.4; // float
$east = 3.4; // float
$west = 3.4; // float

try {
    $result = $apiInstance->redfinSearchProperties($location, $page, $sort, $price_min, $price_max, $beds_min, $baths_min, $home_type, $sqft_min, $sqft_max, $lot_min, $lot_max, $year_built_min, $year_built_max, $max_days_on_market, $north, $south, $east, $west);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedfinApi->redfinSearchProperties: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| City/state, ZIP, address or neighborhood | |
| **page** | **int**|  | [optional] [default to 1] |
| **sort** | **string**| relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths | [optional] |
| **price_min** | **int**|  | [optional] |
| **price_max** | **int**|  | [optional] |
| **beds_min** | **int**|  | [optional] |
| **baths_min** | **float**|  | [optional] |
| **home_type** | **string**| house|condo|townhouse|multi_family|land|mobile|coop|other | [optional] |
| **sqft_min** | **int**|  | [optional] |
| **sqft_max** | **int**|  | [optional] |
| **lot_min** | **int**|  | [optional] |
| **lot_max** | **int**|  | [optional] |
| **year_built_min** | **int**|  | [optional] |
| **year_built_max** | **int**|  | [optional] |
| **max_days_on_market** | **int**|  | [optional] |
| **north** | **float**| Map bounds for tiling past the cap | [optional] |
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

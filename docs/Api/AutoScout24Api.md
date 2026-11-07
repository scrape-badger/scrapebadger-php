# ScrapeBadger\AutoScout24Api

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**autoscout24CheckAutoscout24Health()**](AutoScout24Api.md#autoscout24CheckAutoscout24Health) | **GET** /v1/autoscout24/health | Check AutoScout24 health |
| [**autoscout24GetListing()**](AutoScout24Api.md#autoscout24GetListing) | **GET** /v1/autoscout24/listing | Get listing |
| [**autoscout24ListMarkets()**](AutoScout24Api.md#autoscout24ListMarkets) | **GET** /v1/autoscout24/markets | List markets |
| [**autoscout24ListSearchFilters()**](AutoScout24Api.md#autoscout24ListSearchFilters) | **GET** /v1/autoscout24/filters | List search filters |
| [**autoscout24SearchVehicles()**](AutoScout24Api.md#autoscout24SearchVehicles) | **GET** /v1/autoscout24/search | Search vehicles |


## `autoscout24CheckAutoscout24Health()`

```php
autoscout24CheckAutoscout24Health(): mixed
```

Check AutoScout24 health

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AutoScout24Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->autoscout24CheckAutoscout24Health();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutoScout24Api->autoscout24CheckAutoscout24Health: ', $e->getMessage(), PHP_EOL;
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

## `autoscout24GetListing()`

```php
autoscout24GetListing($url, $listing_id, $market): \ScrapeBadger\Model\AutoScout24ListingResponse
```

Get listing

Full public vehicle specifications, equipment, photos, price and seller data.  Exactly one of url or listing_id is required. Supported markets match /markets. Successful detail costs 10 credits; removed or missing listings return an unbilled 404. Invalid inputs return 422 and source failures 503.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AutoScout24Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$url = 'url_example'; // string | Full HTTPS listing URL from search results. Supply url or listing_id, not both.
$listing_id = 'listing_id_example'; // string | Listing UUID from search results; requires no SEO slug.
$market = 'market_example'; // string | Inferred from URL, otherwise de. Explicit market must match the URL host.

try {
    $result = $apiInstance->autoscout24GetListing($url, $listing_id, $market);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutoScout24Api->autoscout24GetListing: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **url** | **string**| Full HTTPS listing URL from search results. Supply url or listing_id, not both. | [optional] |
| **listing_id** | **string**| Listing UUID from search results; requires no SEO slug. | [optional] |
| **market** | **string**| Inferred from URL, otherwise de. Explicit market must match the URL host. | [optional] |

### Return type

[**\ScrapeBadger\Model\AutoScout24ListingResponse**](../Model/AutoScout24ListingResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `autoscout24ListMarkets()`

```php
autoscout24ListMarkets(): \ScrapeBadger\Model\AutoScout24MarketsResponse
```

List markets

Verified marketplaces, domains, languages and currency. Free reference endpoint.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AutoScout24Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->autoscout24ListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutoScout24Api->autoscout24ListMarkets: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ScrapeBadger\Model\AutoScout24MarketsResponse**](../Model/AutoScout24MarketsResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `autoscout24ListSearchFilters()`

```php
autoscout24ListSearchFilters($market, $make): \ScrapeBadger\Model\AutoScout24FiltersResponse
```

List search filters

Current native make, model and vehicle filter options. Set make for its models.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AutoScout24Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$market = 'de'; // string
$make = 'make_example'; // string

try {
    $result = $apiInstance->autoscout24ListSearchFilters($market, $make);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutoScout24Api->autoscout24ListSearchFilters: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **market** | **string**|  | [optional] [default to &#39;de&#39;] |
| **make** | **string**|  | [optional] |

### Return type

[**\ScrapeBadger\Model\AutoScout24FiltersResponse**](../Model/AutoScout24FiltersResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `autoscout24SearchVehicles()`

```php
autoscout24SearchVehicles($market, $make, $model, $price_min, $price_max, $mileage_min, $mileage_max, $year_min, $year_max, $power_min, $power_max, $fuel_type, $transmission, $body_type, $seller_type, $condition, $zip, $radius, $sort_by, $page): \ScrapeBadger\Model\AutoScout24SearchResponse
```

Search vehicles

Search live vehicle cards, seller/location information and current filter taxonomy.  Browsing is capped at 200 pages (normally 20 cards each). Narrow the query to reach more inventory. Empty results cost zero credits. Pass a result's url or id to /listing for its full specifications and equipment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AutoScout24Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$market = 'de'; // string
$make = 'make_example'; // string | Native make slug, e.g. volkswagen or bmw.
$model = 'model_example'; // string | Native model slug, e.g. golf. Requires make.
$price_min = 56; // int
$price_max = 56; // int
$mileage_min = 56; // int | Kilometres.
$mileage_max = 56; // int
$year_min = 56; // int
$year_max = 56; // int
$power_min = 56; // int | Engine power in kW.
$power_max = 56; // int
$fuel_type = 'fuel_type_example'; // string
$transmission = 'transmission_example'; // string
$body_type = 'body_type_example'; // string
$seller_type = 'seller_type_example'; // string
$condition = 'condition_example'; // string
$zip = 'zip_example'; // string | Postal code in the requested market.
$radius = 56; // int | Kilometres; requires zip.
$sort_by = 'best_match'; // string
$page = 1; // int

try {
    $result = $apiInstance->autoscout24SearchVehicles($market, $make, $model, $price_min, $price_max, $mileage_min, $mileage_max, $year_min, $year_max, $power_min, $power_max, $fuel_type, $transmission, $body_type, $seller_type, $condition, $zip, $radius, $sort_by, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutoScout24Api->autoscout24SearchVehicles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **market** | **string**|  | [optional] [default to &#39;de&#39;] |
| **make** | **string**| Native make slug, e.g. volkswagen or bmw. | [optional] |
| **model** | **string**| Native model slug, e.g. golf. Requires make. | [optional] |
| **price_min** | **int**|  | [optional] |
| **price_max** | **int**|  | [optional] |
| **mileage_min** | **int**| Kilometres. | [optional] |
| **mileage_max** | **int**|  | [optional] |
| **year_min** | **int**|  | [optional] |
| **year_max** | **int**|  | [optional] |
| **power_min** | **int**| Engine power in kW. | [optional] |
| **power_max** | **int**|  | [optional] |
| **fuel_type** | **string**|  | [optional] |
| **transmission** | **string**|  | [optional] |
| **body_type** | **string**|  | [optional] |
| **seller_type** | **string**|  | [optional] |
| **condition** | **string**|  | [optional] |
| **zip** | **string**| Postal code in the requested market. | [optional] |
| **radius** | **int**| Kilometres; requires zip. | [optional] |
| **sort_by** | **string**|  | [optional] [default to &#39;best_match&#39;] |
| **page** | **int**|  | [optional] [default to 1] |

### Return type

[**\ScrapeBadger\Model\AutoScout24SearchResponse**](../Model/AutoScout24SearchResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

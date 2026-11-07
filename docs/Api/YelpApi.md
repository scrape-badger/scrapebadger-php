# ScrapeBadger\YelpApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**yelpListMarkets()**](YelpApi.md#yelpListMarkets) | **GET** /v1/yelp/markets | List markets |
| [**yelpSearchBusinesses()**](YelpApi.md#yelpSearchBusinesses) | **GET** /v1/yelp/search | Search businesses |


## `yelpListMarkets()`

```php
yelpListMarkets(): \ScrapeBadger\Model\YelpMarketsResponse
```

List markets

Yelp sites this API verifiably searches. Free.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YelpApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->yelpListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YelpApi->yelpListMarkets: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ScrapeBadger\Model\YelpMarketsResponse**](../Model/YelpMarketsResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `yelpSearchBusinesses()`

```php
yelpSearchBusinesses($location, $query, $market, $category, $sort_by, $price, $features, $page): \ScrapeBadger\Model\YelpSearchResponse
```

Search businesses

Ranked Yelp businesses for a location, with ads kept separate. 15 credits; empty results free.  Ten businesses per page, pages 1-11. Narrow the location, category or filters to reach more businesses. Business detail and reviews are not part of this API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\YelpApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | Where to search, as typed into Yelp: city, neighbourhood, address or postcode.
$query = 'query_example'; // string | What to search for (e.g. pizza, plumbers). Optional when category is set.
$market = 'us'; // string | Yelp site to search; see /markets.
$category = 'category_example'; // string | Yelp category alias, e.g. pizza, coffee, plumbing.
$sort_by = 'recommended'; // string
$price = 'price_example'; // string | Comma-separated price levels 1-4 ($ to $$$$).
$features = 'features_example'; // string | Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible.
$page = 1; // int | 1-based page, ten businesses each; pages 1-11.

try {
    $result = $apiInstance->yelpSearchBusinesses($location, $query, $market, $category, $sort_by, $price, $features, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YelpApi->yelpSearchBusinesses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| Where to search, as typed into Yelp: city, neighbourhood, address or postcode. | |
| **query** | **string**| What to search for (e.g. pizza, plumbers). Optional when category is set. | [optional] |
| **market** | **string**| Yelp site to search; see /markets. | [optional] [default to &#39;us&#39;] |
| **category** | **string**| Yelp category alias, e.g. pizza, coffee, plumbing. | [optional] |
| **sort_by** | **string**|  | [optional] [default to &#39;recommended&#39;] |
| **price** | **string**| Comma-separated price levels 1-4 ($ to $$$$). | [optional] |
| **features** | **string**| Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible. | [optional] |
| **page** | **int**| 1-based page, ten businesses each; pages 1-11. | [optional] [default to 1] |

### Return type

[**\ScrapeBadger\Model\YelpSearchResponse**](../Model/YelpSearchResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

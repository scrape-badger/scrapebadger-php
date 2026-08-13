# ScrapeBadger\AirbnbApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**airbnbAirbnbScraperHealthCheck()**](AirbnbApi.md#airbnbAirbnbScraperHealthCheck) | **GET** /v1/airbnb/health | Airbnb scraper health check |
| [**airbnbAirbnbScraperHealthCheckHead()**](AirbnbApi.md#airbnbAirbnbScraperHealthCheckHead) | **HEAD** /v1/airbnb/health | Airbnb scraper health check |
| [**airbnbGetAvailabilityCalendar()**](AirbnbApi.md#airbnbGetAvailabilityCalendar) | **GET** /v1/airbnb/listings/{room_id}/calendar | Get availability calendar |
| [**airbnbGetExperienceDetail()**](AirbnbApi.md#airbnbGetExperienceDetail) | **GET** /v1/airbnb/experiences/{experience_id} | Get experience detail |
| [**airbnbGetListingDetail()**](AirbnbApi.md#airbnbGetListingDetail) | **GET** /v1/airbnb/listings/{room_id} | Get listing detail |
| [**airbnbGetListingReviews()**](AirbnbApi.md#airbnbGetListingReviews) | **GET** /v1/airbnb/listings/{room_id}/reviews | Get listing reviews |
| [**airbnbSearchExperiences()**](AirbnbApi.md#airbnbSearchExperiences) | **GET** /v1/airbnb/experiences | Search experiences |
| [**airbnbSearchStays()**](AirbnbApi.md#airbnbSearchStays) | **GET** /v1/airbnb/search | Search stays |


## `airbnbAirbnbScraperHealthCheck()`

```php
airbnbAirbnbScraperHealthCheck(): mixed
```

Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AirbnbApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->airbnbAirbnbScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AirbnbApi->airbnbAirbnbScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `airbnbAirbnbScraperHealthCheckHead()`

```php
airbnbAirbnbScraperHealthCheckHead(): mixed
```

Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AirbnbApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->airbnbAirbnbScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AirbnbApi->airbnbAirbnbScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `airbnbGetAvailabilityCalendar()`

```php
airbnbGetAvailabilityCalendar($room_id, $month, $year, $months, $currency, $locale): mixed
```

Get availability calendar

Day-by-day availability for up to 12 months: bookable, check-in/out windows and min/max nights per date.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AirbnbApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$room_id = 'room_id_example'; // string
$month = 1; // int | Start month (1-12)
$year = 2026; // int | Start year
$months = 12; // int | Number of months (max 12)
$currency = 'currency_example'; // string
$locale = 'locale_example'; // string

try {
    $result = $apiInstance->airbnbGetAvailabilityCalendar($room_id, $month, $year, $months, $currency, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AirbnbApi->airbnbGetAvailabilityCalendar: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **room_id** | **string**|  | |
| **month** | **int**| Start month (1-12) | [optional] [default to 1] |
| **year** | **int**| Start year | [optional] [default to 2026] |
| **months** | **int**| Number of months (max 12) | [optional] [default to 12] |
| **currency** | **string**|  | [optional] |
| **locale** | **string**|  | [optional] |

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

## `airbnbGetExperienceDetail()`

```php
airbnbGetExperienceDetail($experience_id, $adults, $children, $infants, $currency, $locale): mixed
```

Get experience detail

Full detail for one experience: description, rating, host, location and photos.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AirbnbApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$experience_id = 'experience_id_example'; // string
$adults = 1; // int
$children = 0; // int
$infants = 0; // int
$currency = 'currency_example'; // string
$locale = 'locale_example'; // string

try {
    $result = $apiInstance->airbnbGetExperienceDetail($experience_id, $adults, $children, $infants, $currency, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AirbnbApi->airbnbGetExperienceDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **experience_id** | **string**|  | |
| **adults** | **int**|  | [optional] [default to 1] |
| **children** | **int**|  | [optional] [default to 0] |
| **infants** | **int**|  | [optional] [default to 0] |
| **currency** | **string**|  | [optional] |
| **locale** | **string**|  | [optional] |

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

## `airbnbGetListingDetail()`

```php
airbnbGetListingDetail($room_id, $adults, $currency, $locale): mixed
```

Get listing detail

Full detail for one listing: amenities, house rules, host, ratings, coordinates and photos.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AirbnbApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$room_id = 'room_id_example'; // string
$adults = 1; // int
$currency = 'currency_example'; // string
$locale = 'locale_example'; // string

try {
    $result = $apiInstance->airbnbGetListingDetail($room_id, $adults, $currency, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AirbnbApi->airbnbGetListingDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **room_id** | **string**|  | |
| **adults** | **int**|  | [optional] [default to 1] |
| **currency** | **string**|  | [optional] |
| **locale** | **string**|  | [optional] |

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

## `airbnbGetListingReviews()`

```php
airbnbGetListingReviews($room_id, $limit, $offset, $sort, $currency, $locale): mixed
```

Get listing reviews

Paginated guest reviews with reviewer, rating, date, text and host response.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AirbnbApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$room_id = 'room_id_example'; // string
$limit = 24; // int
$offset = 0; // int
$sort = 'MOST_RECENT'; // string | MOST_RECENT | RATING_DESC | RATING_ASC
$currency = 'currency_example'; // string
$locale = 'locale_example'; // string

try {
    $result = $apiInstance->airbnbGetListingReviews($room_id, $limit, $offset, $sort, $currency, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AirbnbApi->airbnbGetListingReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **room_id** | **string**|  | |
| **limit** | **int**|  | [optional] [default to 24] |
| **offset** | **int**|  | [optional] [default to 0] |
| **sort** | **string**| MOST_RECENT | RATING_DESC | RATING_ASC | [optional] [default to &#39;MOST_RECENT&#39;] |
| **currency** | **string**|  | [optional] |
| **locale** | **string**|  | [optional] |

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

## `airbnbSearchExperiences()`

```php
airbnbSearchExperiences($location, $cursor, $currency, $locale): mixed
```

Search experiences

Search Airbnb Experiences by location.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AirbnbApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | Free-text place, e.g. 'Rome, Italy'
$cursor = 'cursor_example'; // string | next_page_cursor from a prior response
$currency = 'currency_example'; // string
$locale = 'locale_example'; // string

try {
    $result = $apiInstance->airbnbSearchExperiences($location, $cursor, $currency, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AirbnbApi->airbnbSearchExperiences: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| Free-text place, e.g. &#39;Rome, Italy&#39; | |
| **cursor** | **string**| next_page_cursor from a prior response | [optional] |
| **currency** | **string**|  | [optional] |
| **locale** | **string**|  | [optional] |

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

## `airbnbSearchStays()`

```php
airbnbSearchStays($location, $ne_lat, $ne_lng, $sw_lat, $sw_lng, $check_in, $check_out, $adults, $children, $infants, $pets, $price_min, $price_max, $min_bedrooms, $min_beds, $min_bathrooms, $room_type, $cursor, $limit, $currency, $locale): mixed
```

Search stays

Search Airbnb stays by place name and/or map bounding box, with dates, guests, price and property filters. Paginate with the `cursor`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AirbnbApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | Free-text place, e.g. 'Paris, France'
$ne_lat = 3.4; // float | Map bounding-box NE latitude
$ne_lng = 3.4; // float | Map bounding-box NE longitude
$sw_lat = 3.4; // float | Map bounding-box SW latitude
$sw_lng = 3.4; // float | Map bounding-box SW longitude
$check_in = 'check_in_example'; // string | Check-in date YYYY-MM-DD
$check_out = 'check_out_example'; // string | Check-out date YYYY-MM-DD
$adults = 1; // int
$children = 0; // int
$infants = 0; // int
$pets = 0; // int
$price_min = 56; // int
$price_max = 56; // int
$min_bedrooms = 56; // int
$min_beds = 56; // int
$min_bathrooms = 56; // int
$room_type = 'room_type_example'; // string | e.g. 'Entire home/apt', 'Private room'
$cursor = 'cursor_example'; // string | next_page_cursor from a prior response
$limit = 18; // int
$currency = 'currency_example'; // string | ISO currency, e.g. USD, EUR
$locale = 'locale_example'; // string | Locale, e.g. en, fr

try {
    $result = $apiInstance->airbnbSearchStays($location, $ne_lat, $ne_lng, $sw_lat, $sw_lng, $check_in, $check_out, $adults, $children, $infants, $pets, $price_min, $price_max, $min_bedrooms, $min_beds, $min_bathrooms, $room_type, $cursor, $limit, $currency, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AirbnbApi->airbnbSearchStays: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| Free-text place, e.g. &#39;Paris, France&#39; | [optional] |
| **ne_lat** | **float**| Map bounding-box NE latitude | [optional] |
| **ne_lng** | **float**| Map bounding-box NE longitude | [optional] |
| **sw_lat** | **float**| Map bounding-box SW latitude | [optional] |
| **sw_lng** | **float**| Map bounding-box SW longitude | [optional] |
| **check_in** | **string**| Check-in date YYYY-MM-DD | [optional] |
| **check_out** | **string**| Check-out date YYYY-MM-DD | [optional] |
| **adults** | **int**|  | [optional] [default to 1] |
| **children** | **int**|  | [optional] [default to 0] |
| **infants** | **int**|  | [optional] [default to 0] |
| **pets** | **int**|  | [optional] [default to 0] |
| **price_min** | **int**|  | [optional] |
| **price_max** | **int**|  | [optional] |
| **min_bedrooms** | **int**|  | [optional] |
| **min_beds** | **int**|  | [optional] |
| **min_bathrooms** | **int**|  | [optional] |
| **room_type** | **string**| e.g. &#39;Entire home/apt&#39;, &#39;Private room&#39; | [optional] |
| **cursor** | **string**| next_page_cursor from a prior response | [optional] |
| **limit** | **int**|  | [optional] [default to 18] |
| **currency** | **string**| ISO currency, e.g. USD, EUR | [optional] |
| **locale** | **string**| Locale, e.g. en, fr | [optional] |

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

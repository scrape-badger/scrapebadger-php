# ScrapeBadger\BookingApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bookingBookingScraperHealthCheck()**](BookingApi.md#bookingBookingScraperHealthCheck) | **GET** /v1/booking/health | Booking scraper health check |
| [**bookingBookingScraperHealthCheckHead()**](BookingApi.md#bookingBookingScraperHealthCheckHead) | **HEAD** /v1/booking/health | Booking scraper health check |
| [**bookingGetPropertyDetail()**](BookingApi.md#bookingGetPropertyDetail) | **GET** /v1/booking/properties/{country_code}/{slug} | Get property detail |
| [**bookingGetPropertyReviews()**](BookingApi.md#bookingGetPropertyReviews) | **GET** /v1/booking/properties/{country_code}/{slug}/reviews | Get property reviews |
| [**bookingGetRoomTypesAndLiveRates()**](BookingApi.md#bookingGetRoomTypesAndLiveRates) | **GET** /v1/booking/properties/{country_code}/{slug}/rooms | Get room types and live rates |
| [**bookingSearchDestinations()**](BookingApi.md#bookingSearchDestinations) | **GET** /v1/booking/destinations | Search destinations |
| [**bookingSearchProperties()**](BookingApi.md#bookingSearchProperties) | **GET** /v1/booking/search | Search properties |


## `bookingBookingScraperHealthCheck()`

```php
bookingBookingScraperHealthCheck(): mixed
```

Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BookingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->bookingBookingScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BookingApi->bookingBookingScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `bookingBookingScraperHealthCheckHead()`

```php
bookingBookingScraperHealthCheckHead(): mixed
```

Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BookingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->bookingBookingScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BookingApi->bookingBookingScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `bookingGetPropertyDetail()`

```php
bookingGetPropertyDetail($country_code, $slug, $photos, $questions, $language): mixed
```

Get property detail

Full detail for one property: description, address and coordinates, star rating, review score with per-category breakdown, facilities, house rules, room types with occupancy and beds, photos and guest Q&A.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BookingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country_code = 'country_code_example'; // string | Two-letter country code, e.g. 'it'
$slug = 'slug_example'; // string | Booking page name, e.g. 'hotel-artemide'
$photos = 40; // int | Gallery photos to return
$questions = 10; // int | Guest Q&A pairs to return
$language = 'language_example'; // string | Locale, e.g. en-us, fr

try {
    $result = $apiInstance->bookingGetPropertyDetail($country_code, $slug, $photos, $questions, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BookingApi->bookingGetPropertyDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **country_code** | **string**| Two-letter country code, e.g. &#39;it&#39; | |
| **slug** | **string**| Booking page name, e.g. &#39;hotel-artemide&#39; | |
| **photos** | **int**| Gallery photos to return | [optional] [default to 40] |
| **questions** | **int**| Guest Q&amp;A pairs to return | [optional] [default to 10] |
| **language** | **string**| Locale, e.g. en-us, fr | [optional] |

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

## `bookingGetPropertyReviews()`

```php
bookingGetPropertyReviews($country_code, $slug, $limit, $offset, $sort, $review_language, $guest_type, $language): mixed
```

Get property reviews

Paginated guest reviews with score, positive and negative text, stay dates, room type, guest country and type, photos and the partner's reply.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BookingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country_code = 'country_code_example'; // string | Two-letter country code, e.g. 'it'
$slug = 'slug_example'; // string | Booking page name, e.g. 'hotel-artemide'
$limit = 25; // int
$offset = 0; // int
$sort = 'MOST_RELEVANT'; // string | MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC
$review_language = 'review_language_example'; // string | Only reviews written in this language, e.g. 'fr'
$guest_type = 'guest_type_example'; // string | FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS
$language = 'language_example'; // string | Locale for labels, e.g. en-us

try {
    $result = $apiInstance->bookingGetPropertyReviews($country_code, $slug, $limit, $offset, $sort, $review_language, $guest_type, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BookingApi->bookingGetPropertyReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **country_code** | **string**| Two-letter country code, e.g. &#39;it&#39; | |
| **slug** | **string**| Booking page name, e.g. &#39;hotel-artemide&#39; | |
| **limit** | **int**|  | [optional] [default to 25] |
| **offset** | **int**|  | [optional] [default to 0] |
| **sort** | **string**| MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC | [optional] [default to &#39;MOST_RELEVANT&#39;] |
| **review_language** | **string**| Only reviews written in this language, e.g. &#39;fr&#39; | [optional] |
| **guest_type** | **string**| FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS | [optional] |
| **language** | **string**| Locale for labels, e.g. en-us | [optional] |

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

## `bookingGetRoomTypesAndLiveRates()`

```php
bookingGetRoomTypesAndLiveRates($country_code, $slug, $checkin, $checkout, $adults, $children, $rooms, $currency, $language): mixed
```

Get room types and live rates

Every room type at one property with every rate bookable on it for the given dates — price, price before discount, price per night, discounts and badges — plus per-room facilities, bed layouts, occupancy and photos. /search returns only the cheapest rate per property; this returns the whole table.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BookingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country_code = 'country_code_example'; // string | Two-letter country code, e.g. 'it'
$slug = 'slug_example'; // string | Booking page name, e.g. 'hotel-artemide'
$checkin = 'checkin_example'; // string | Check-in date YYYY-MM-DD
$checkout = 'checkout_example'; // string | Check-out date YYYY-MM-DD
$adults = 2; // int
$children = 'children_example'; // string | Comma-separated children ages, e.g. '4,9'
$rooms = 1; // int
$currency = 'currency_example'; // string | ISO currency, e.g. EUR, USD, GBP
$language = 'language_example'; // string | Locale, e.g. en-us, fr, de

try {
    $result = $apiInstance->bookingGetRoomTypesAndLiveRates($country_code, $slug, $checkin, $checkout, $adults, $children, $rooms, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BookingApi->bookingGetRoomTypesAndLiveRates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **country_code** | **string**| Two-letter country code, e.g. &#39;it&#39; | |
| **slug** | **string**| Booking page name, e.g. &#39;hotel-artemide&#39; | |
| **checkin** | **string**| Check-in date YYYY-MM-DD | |
| **checkout** | **string**| Check-out date YYYY-MM-DD | |
| **adults** | **int**|  | [optional] [default to 2] |
| **children** | **string**| Comma-separated children ages, e.g. &#39;4,9&#39; | [optional] |
| **rooms** | **int**|  | [optional] [default to 1] |
| **currency** | **string**| ISO currency, e.g. EUR, USD, GBP | [optional] |
| **language** | **string**| Locale, e.g. en-us, fr, de | [optional] |

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

## `bookingSearchDestinations()`

```php
bookingSearchDestinations($query, $limit, $language): mixed
```

Search destinations

Resolve a place name to Booking's `dest_id`/`dest_type`, with coordinates and country — feed the pair back into /search for an exact match.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BookingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Free-text place, e.g. 'amsterd'
$limit = 8; // int
$language = 'language_example'; // string | Locale, e.g. en-us, fr

try {
    $result = $apiInstance->bookingSearchDestinations($query, $limit, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BookingApi->bookingSearchDestinations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Free-text place, e.g. &#39;amsterd&#39; | |
| **limit** | **int**|  | [optional] [default to 8] |
| **language** | **string**| Locale, e.g. en-us, fr | [optional] |

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

## `bookingSearchProperties()`

```php
bookingSearchProperties($location, $dest_id, $dest_type, $checkin, $checkout, $adults, $children, $rooms, $offset, $limit, $sort, $filters, $currency, $language): mixed
```

Search properties

Search Booking.com properties by destination, with dates, occupancy, sorting and filters. Returns prices, review scores, coordinates, room configuration and photos. Paginate with `offset`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BookingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$location = 'location_example'; // string | Free-text destination, e.g. 'Rome'
$dest_id = 56; // int | Exact destination id (ufi) from /destinations
$dest_type = 'NO_DEST_TYPE'; // string | Destination type, e.g. CITY
$checkin = 'checkin_example'; // string | Check-in date YYYY-MM-DD
$checkout = 'checkout_example'; // string | Check-out date YYYY-MM-DD
$adults = 2; // int
$children = 'children_example'; // string | Comma-separated children ages, e.g. '4,9'
$rooms = 1; // int
$offset = 0; // int | Result offset for pagination
$limit = 25; // int
$sort = 'sort_example'; // string | popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh
$filters = 'filters_example'; // string | Semicolon-separated Booking filter ids, e.g. 'class=4'
$currency = 'currency_example'; // string | ISO currency, e.g. EUR, USD, GBP
$language = 'language_example'; // string | Locale, e.g. en-us, fr, de, es

try {
    $result = $apiInstance->bookingSearchProperties($location, $dest_id, $dest_type, $checkin, $checkout, $adults, $children, $rooms, $offset, $limit, $sort, $filters, $currency, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BookingApi->bookingSearchProperties: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location** | **string**| Free-text destination, e.g. &#39;Rome&#39; | [optional] |
| **dest_id** | **int**| Exact destination id (ufi) from /destinations | [optional] |
| **dest_type** | **string**| Destination type, e.g. CITY | [optional] [default to &#39;NO_DEST_TYPE&#39;] |
| **checkin** | **string**| Check-in date YYYY-MM-DD | [optional] |
| **checkout** | **string**| Check-out date YYYY-MM-DD | [optional] |
| **adults** | **int**|  | [optional] [default to 2] |
| **children** | **string**| Comma-separated children ages, e.g. &#39;4,9&#39; | [optional] |
| **rooms** | **int**|  | [optional] [default to 1] |
| **offset** | **int**| Result offset for pagination | [optional] [default to 0] |
| **limit** | **int**|  | [optional] [default to 25] |
| **sort** | **string**| popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh | [optional] |
| **filters** | **string**| Semicolon-separated Booking filter ids, e.g. &#39;class&#x3D;4&#39; | [optional] |
| **currency** | **string**| ISO currency, e.g. EUR, USD, GBP | [optional] |
| **language** | **string**| Locale, e.g. en-us, fr, de, es | [optional] |

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

# ScrapeBadger\GoogleApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**googleGetAuthorCitationsPerYearChart()**](GoogleApi.md#googleGetAuthorCitationsPerYearChart) | **GET** /v1/google/scholar/author/citation | Get author citations-per-year chart |
| [**googleGetBusinessPosts()**](GoogleApi.md#googleGetBusinessPosts) | **GET** /v1/google/maps/posts | Get business posts |
| [**googleGetCitationFormatsForAScholarPaper()**](GoogleApi.md#googleGetCitationFormatsForAScholarPaper) | **GET** /v1/google/scholar/cite | Get citation formats for a Scholar paper |
| [**googleGetPlaceDetails()**](GoogleApi.md#googleGetPlaceDetails) | **GET** /v1/google/maps/place | Get place details |
| [**googleGetPlacePhotos()**](GoogleApi.md#googleGetPlacePhotos) | **GET** /v1/google/maps/photos | Get place photos |
| [**googleGetPlaceReviews()**](GoogleApi.md#googleGetPlaceReviews) | **GET** /v1/google/maps/reviews | Get place reviews |
| [**googleGetScholarAuthorProfile()**](GoogleApi.md#googleGetScholarAuthorProfile) | **GET** /v1/google/scholar/author | Get Scholar author profile |
| [**googleGetStockIndexQuote()**](GoogleApi.md#googleGetStockIndexQuote) | **GET** /v1/google/finance/quote | Get stock/index quote |
| [**googleGoogleAiModeSearch()**](GoogleApi.md#googleGoogleAiModeSearch) | **GET** /v1/google/ai-mode/search | Google AI Mode search |
| [**googleGoogleAiOverviewInlineSerpBlock()**](GoogleApi.md#googleGoogleAiOverviewInlineSerpBlock) | **GET** /v1/google/ai-overview | Google AI Overview (inline SERP block) |
| [**googleGoogleFlightsCalendarCheapestFarePerDate()**](GoogleApi.md#googleGoogleFlightsCalendarCheapestFarePerDate) | **GET** /v1/google/flights/calendar | Google Flights calendar — cheapest fare per date |
| [**googleGoogleFlightsSearch()**](GoogleApi.md#googleGoogleFlightsSearch) | **GET** /v1/google/flights/search | Google Flights search |
| [**googleGoogleLensVisualSearch()**](GoogleApi.md#googleGoogleLensVisualSearch) | **GET** /v1/google/lens/search | Google Lens visual search |
| [**googleGoogleScraperHealthCheck()**](GoogleApi.md#googleGoogleScraperHealthCheck) | **GET** /v1/google/health | Google scraper health check |
| [**googleGoogleScraperHealthCheckHead()**](GoogleApi.md#googleGoogleScraperHealthCheckHead) | **HEAD** /v1/google/health | Google scraper health check |
| [**googleGoogleSearchSuggestions()**](GoogleApi.md#googleGoogleSearchSuggestions) | **GET** /v1/google/autocomplete | Google search suggestions |
| [**googleGoogleShortsSearch()**](GoogleApi.md#googleGoogleShortsSearch) | **GET** /v1/google/shorts/search | Google Shorts search |
| [**googleGoogleWebSearch()**](GoogleApi.md#googleGoogleWebSearch) | **GET** /v1/google/search | Google web search |
| [**googleHotelDetails()**](GoogleApi.md#googleHotelDetails) | **GET** /v1/google/hotels/details | Hotel details |
| [**googleImmersiveProductDetail()**](GoogleApi.md#googleImmersiveProductDetail) | **GET** /v1/google/products/detail | Immersive product detail |
| [**googleInterestByRegion()**](GoogleApi.md#googleInterestByRegion) | **GET** /v1/google/trends/regions | Interest by region |
| [**googleInterestOverTime()**](GoogleApi.md#googleInterestOverTime) | **GET** /v1/google/trends/interest | Interest over time |
| [**googleMultiSellerOffersByBarcode()**](GoogleApi.md#googleMultiSellerOffersByBarcode) | **GET** /v1/google/shopping/offers | Multi-seller offers by barcode |
| [**googleNewsByTopic()**](GoogleApi.md#googleNewsByTopic) | **GET** /v1/google/news/topics | News by topic |
| [**googlePatentDetails()**](GoogleApi.md#googlePatentDetails) | **GET** /v1/google/patents/detail | Patent details |
| [**googleRelatedTopicsQueries()**](GoogleApi.md#googleRelatedTopicsQueries) | **GET** /v1/google/trends/related | Related topics &amp; queries |
| [**googleSearchGoogleImages()**](GoogleApi.md#googleSearchGoogleImages) | **GET** /v1/google/images/search | Search Google Images |
| [**googleSearchGoogleJobs()**](GoogleApi.md#googleSearchGoogleJobs) | **GET** /v1/google/jobs/search | Search Google Jobs |
| [**googleSearchGoogleMapsPlaces()**](GoogleApi.md#googleSearchGoogleMapsPlaces) | **GET** /v1/google/maps/search | Search Google Maps places |
| [**googleSearchGoogleNews()**](GoogleApi.md#googleSearchGoogleNews) | **GET** /v1/google/news/search | Search Google News |
| [**googleSearchGoogleScholar()**](GoogleApi.md#googleSearchGoogleScholar) | **GET** /v1/google/scholar/search | Search Google Scholar |
| [**googleSearchGoogleVideos()**](GoogleApi.md#googleSearchGoogleVideos) | **GET** /v1/google/videos/search | Search Google Videos |
| [**googleSearchHotels()**](GoogleApi.md#googleSearchHotels) | **GET** /v1/google/hotels/search | Search hotels |
| [**googleSearchPatents()**](GoogleApi.md#googleSearchPatents) | **GET** /v1/google/patents/search | Search patents |
| [**googleSearchProducts()**](GoogleApi.md#googleSearchProducts) | **GET** /v1/google/shopping/search | Search products |
| [**googleSearchScholarAuthorProfiles()**](GoogleApi.md#googleSearchScholarAuthorProfiles) | **GET** /v1/google/scholar/profiles | Search Scholar author profiles |
| [**googleTrendingNews()**](GoogleApi.md#googleTrendingNews) | **GET** /v1/google/news/trending | Trending news |
| [**googleTrendingSearches()**](GoogleApi.md#googleTrendingSearches) | **GET** /v1/google/trends/trending | Trending searches |
| [**googleTrendsTopicAutocomplete()**](GoogleApi.md#googleTrendsTopicAutocomplete) | **GET** /v1/google/trends/autocomplete | Trends topic autocomplete |


## `googleGetAuthorCitationsPerYearChart()`

```php
googleGetAuthorCitationsPerYearChart($author_id, $hl): mixed
```

Get author citations-per-year chart

Return the citations-per-year chart for a Google Scholar author.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$author_id = 'author_id_example'; // string | Scholar user ID
$hl = 'en'; // string | Language code

try {
    $result = $apiInstance->googleGetAuthorCitationsPerYearChart($author_id, $hl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGetAuthorCitationsPerYearChart: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **author_id** | **string**| Scholar user ID | |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |

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

## `googleGetBusinessPosts()`

```php
googleGetBusinessPosts($data_id, $next_page_token): mixed
```

Get business posts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$data_id = 'data_id_example'; // string | Maps data ID
$next_page_token = 'next_page_token_example'; // string

try {
    $result = $apiInstance->googleGetBusinessPosts($data_id, $next_page_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGetBusinessPosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **data_id** | **string**| Maps data ID | |
| **next_page_token** | **string**|  | [optional] |

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

## `googleGetCitationFormatsForAScholarPaper()`

```php
googleGetCitationFormatsForAScholarPaper($q, $hl): mixed
```

Get citation formats for a Scholar paper

Return MLA, APA, Chicago, Harvard, and Vancouver citation formats for a paper.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Cluster ID from a search result
$hl = 'en'; // string | Language code

try {
    $result = $apiInstance->googleGetCitationFormatsForAScholarPaper($q, $hl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGetCitationFormatsForAScholarPaper: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Cluster ID from a search result | |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |

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

## `googleGetPlaceDetails()`

```php
googleGetPlaceDetails($place_id, $data_id, $hl, $gl): mixed
```

Get place details

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$place_id = 'place_id_example'; // string
$data_id = 'data_id_example'; // string
$hl = 'en'; // string
$gl = 'us'; // string

try {
    $result = $apiInstance->googleGetPlaceDetails($place_id, $data_id, $hl, $gl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGetPlaceDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **place_id** | **string**|  | [optional] |
| **data_id** | **string**|  | [optional] |
| **hl** | **string**|  | [optional] [default to &#39;en&#39;] |
| **gl** | **string**|  | [optional] [default to &#39;us&#39;] |

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

## `googleGetPlacePhotos()`

```php
googleGetPlacePhotos($data_id, $hl, $next_page_token): mixed
```

Get place photos

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$data_id = 'data_id_example'; // string | Maps data ID
$hl = 'en'; // string
$next_page_token = 'next_page_token_example'; // string

try {
    $result = $apiInstance->googleGetPlacePhotos($data_id, $hl, $next_page_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGetPlacePhotos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **data_id** | **string**| Maps data ID | |
| **hl** | **string**|  | [optional] [default to &#39;en&#39;] |
| **next_page_token** | **string**|  | [optional] |

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

## `googleGetPlaceReviews()`

```php
googleGetPlaceReviews($data_id, $sort_by, $hl, $next_page_token, $results): mixed
```

Get place reviews

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$data_id = 'data_id_example'; // string | Maps data ID
$sort_by = 'qualityScore'; // string
$hl = 'en'; // string
$next_page_token = 'next_page_token_example'; // string
$results = 10; // int

try {
    $result = $apiInstance->googleGetPlaceReviews($data_id, $sort_by, $hl, $next_page_token, $results);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGetPlaceReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **data_id** | **string**| Maps data ID | |
| **sort_by** | **string**|  | [optional] [default to &#39;qualityScore&#39;] |
| **hl** | **string**|  | [optional] [default to &#39;en&#39;] |
| **next_page_token** | **string**|  | [optional] |
| **results** | **int**|  | [optional] [default to 10] |

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

## `googleGetScholarAuthorProfile()`

```php
googleGetScholarAuthorProfile($author_id, $hl, $cstart, $pagesize): mixed
```

Get Scholar author profile

Get detailed Google Scholar author profile including articles, stats, co-authors.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$author_id = 'author_id_example'; // string | Scholar user ID (the `user` query parameter)
$hl = 'en'; // string | Language code
$cstart = 0; // int | Articles pagination offset
$pagesize = 20; // int | Articles per page

try {
    $result = $apiInstance->googleGetScholarAuthorProfile($author_id, $hl, $cstart, $pagesize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGetScholarAuthorProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **author_id** | **string**| Scholar user ID (the &#x60;user&#x60; query parameter) | |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **cstart** | **int**| Articles pagination offset | [optional] [default to 0] |
| **pagesize** | **int**| Articles per page | [optional] [default to 20] |

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

## `googleGetStockIndexQuote()`

```php
googleGetStockIndexQuote($q, $hl): mixed
```

Get stock/index quote

Get a stock or index quote from Google Finance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Ticker and exchange (e.g. \"AAPL:NASDAQ\", \"BTC-USD\")
$hl = 'en'; // string | Language code

try {
    $result = $apiInstance->googleGetStockIndexQuote($q, $hl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGetStockIndexQuote: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Ticker and exchange (e.g. \&quot;AAPL:NASDAQ\&quot;, \&quot;BTC-USD\&quot;) | |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |

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

## `googleGoogleAiModeSearch()`

```php
googleGoogleAiModeSearch($q, $gl, $hl, $include_html): mixed
```

Google AI Mode search

Get AI-generated search results from Google AI Mode.  Returns the structured `text_blocks` (paragraphs, headings, comparison `table` blocks and lists), a flat `references` source list, a compact `markdown` rendering of the whole answer and — unless `include_html` is false — the raw `answer_html` body.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query for AI-generated response
$gl = 'us'; // string | Country code
$hl = 'en'; // string | Language code
$include_html = true; // bool | Include the raw `answer_html` (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured `text_blocks` + `markdown`.

try {
    $result = $apiInstance->googleGoogleAiModeSearch($q, $gl, $hl, $include_html);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGoogleAiModeSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query for AI-generated response | |
| **gl** | **string**| Country code | [optional] [default to &#39;us&#39;] |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **include_html** | **bool**| Include the raw &#x60;answer_html&#x60; (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured &#x60;text_blocks&#x60; + &#x60;markdown&#x60;. | [optional] [default to true] |

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

## `googleGoogleAiOverviewInlineSerpBlock()`

```php
googleGoogleAiOverviewInlineSerpBlock($q, $gl, $hl): mixed
```

Google AI Overview (inline SERP block)

Get the AI Overview block Google renders inline at the top of a SERP.  Deferred overviews (where Google lazy-loads the block via a follow-up ``page_token``) are chased automatically.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query — same shape as a Google Search query
$gl = 'us'; // string | Country code
$hl = 'en'; // string | Language code

try {
    $result = $apiInstance->googleGoogleAiOverviewInlineSerpBlock($q, $gl, $hl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGoogleAiOverviewInlineSerpBlock: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query — same shape as a Google Search query | |
| **gl** | **string**| Country code | [optional] [default to &#39;us&#39;] |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |

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

## `googleGoogleFlightsCalendarCheapestFarePerDate()`

```php
googleGoogleFlightsCalendarCheapestFarePerDate($departure_id, $arrival_id, $outbound_date_from, $outbound_date_to, $trip_type, $trip_length_days, $return_date_from, $return_date_to, $adults, $children, $infants_in_seat, $infants_on_lap, $travel_class, $currency, $gl, $hl): mixed
```

Google Flights calendar — cheapest fare per date

Price a whole range of dates in one call — up to 200 dates per request.  Google Flights' own price graph / date grid: the cheapest fare per departure date instead of one search per date. Prices match `/flights/search` exactly.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$departure_id = 'departure_id_example'; // string | Departure airport IATA code or location ID
$arrival_id = 'arrival_id_example'; // string | Arrival airport IATA code or location ID
$outbound_date_from = 'outbound_date_from_example'; // string | First outbound date to price (YYYY-MM-DD)
$outbound_date_to = 'outbound_date_to_example'; // string | Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode.
$trip_type = 'one_way'; // string | one_way | round_trip
$trip_length_days = 56; // int | Round-trip stay length in nights (price-graph mode). Defaults to 7.
$return_date_from = 'return_date_from_example'; // string | Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only.
$return_date_to = 'return_date_to_example'; // string | Date-grid mode: last return date
$adults = 1; // int
$children = 0; // int
$infants_in_seat = 0; // int
$infants_on_lap = 0; // int
$travel_class = 'economy'; // string
$currency = 'USD'; // string | ISO-4217 currency
$gl = 'us'; // string
$hl = 'en'; // string

try {
    $result = $apiInstance->googleGoogleFlightsCalendarCheapestFarePerDate($departure_id, $arrival_id, $outbound_date_from, $outbound_date_to, $trip_type, $trip_length_days, $return_date_from, $return_date_to, $adults, $children, $infants_in_seat, $infants_on_lap, $travel_class, $currency, $gl, $hl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGoogleFlightsCalendarCheapestFarePerDate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **departure_id** | **string**| Departure airport IATA code or location ID | |
| **arrival_id** | **string**| Arrival airport IATA code or location ID | |
| **outbound_date_from** | **string**| First outbound date to price (YYYY-MM-DD) | |
| **outbound_date_to** | **string**| Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode. | |
| **trip_type** | **string**| one_way | round_trip | [optional] [default to &#39;one_way&#39;] |
| **trip_length_days** | **int**| Round-trip stay length in nights (price-graph mode). Defaults to 7. | [optional] |
| **return_date_from** | **string**| Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only. | [optional] |
| **return_date_to** | **string**| Date-grid mode: last return date | [optional] |
| **adults** | **int**|  | [optional] [default to 1] |
| **children** | **int**|  | [optional] [default to 0] |
| **infants_in_seat** | **int**|  | [optional] [default to 0] |
| **infants_on_lap** | **int**|  | [optional] [default to 0] |
| **travel_class** | **string**|  | [optional] [default to &#39;economy&#39;] |
| **currency** | **string**| ISO-4217 currency | [optional] [default to &#39;USD&#39;] |
| **gl** | **string**|  | [optional] [default to &#39;us&#39;] |
| **hl** | **string**|  | [optional] [default to &#39;en&#39;] |

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

## `googleGoogleFlightsSearch()`

```php
googleGoogleFlightsSearch($departure_id, $arrival_id, $outbound_date, $return_date, $trip_type, $adults, $children, $infants_in_seat, $infants_on_lap, $travel_class, $currency, $gl, $hl, $stops, $max_price, $departure_token): mixed
```

Google Flights search

Search Google Flights for available itineraries.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$departure_id = 'departure_id_example'; // string | Departure airport IATA code or location ID
$arrival_id = 'arrival_id_example'; // string | Arrival airport IATA code or location ID
$outbound_date = 'outbound_date_example'; // string | Outbound date (YYYY-MM-DD)
$return_date = 'return_date_example'; // string | Return date (round-trip only)
$trip_type = 'round_trip'; // string | round_trip | one_way | multi_city
$adults = 1; // int
$children = 0; // int
$infants_in_seat = 0; // int
$infants_on_lap = 0; // int
$travel_class = 'economy'; // string
$currency = 'USD'; // string | ISO-4217 currency
$gl = 'us'; // string
$hl = 'en'; // string
$stops = 'any'; // string
$max_price = 56; // int
$departure_token = 'departure_token_example'; // string | A round-trip offer's departure_token; returns the return-leg flights for that selected outbound (round-trip only).

try {
    $result = $apiInstance->googleGoogleFlightsSearch($departure_id, $arrival_id, $outbound_date, $return_date, $trip_type, $adults, $children, $infants_in_seat, $infants_on_lap, $travel_class, $currency, $gl, $hl, $stops, $max_price, $departure_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGoogleFlightsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **departure_id** | **string**| Departure airport IATA code or location ID | |
| **arrival_id** | **string**| Arrival airport IATA code or location ID | |
| **outbound_date** | **string**| Outbound date (YYYY-MM-DD) | |
| **return_date** | **string**| Return date (round-trip only) | [optional] |
| **trip_type** | **string**| round_trip | one_way | multi_city | [optional] [default to &#39;round_trip&#39;] |
| **adults** | **int**|  | [optional] [default to 1] |
| **children** | **int**|  | [optional] [default to 0] |
| **infants_in_seat** | **int**|  | [optional] [default to 0] |
| **infants_on_lap** | **int**|  | [optional] [default to 0] |
| **travel_class** | **string**|  | [optional] [default to &#39;economy&#39;] |
| **currency** | **string**| ISO-4217 currency | [optional] [default to &#39;USD&#39;] |
| **gl** | **string**|  | [optional] [default to &#39;us&#39;] |
| **hl** | **string**|  | [optional] [default to &#39;en&#39;] |
| **stops** | **string**|  | [optional] [default to &#39;any&#39;] |
| **max_price** | **int**|  | [optional] |
| **departure_token** | **string**| A round-trip offer&#39;s departure_token; returns the return-leg flights for that selected outbound (round-trip only). | [optional] |

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

## `googleGoogleLensVisualSearch()`

```php
googleGoogleLensVisualSearch($url, $query, $country, $language, $gl, $hl, $product, $visual_matches, $exact_matches): mixed
```

Google Lens visual search

Google Lens visual search.  Response carries ``lens_results`` (Scrapingdog parity alias) with ``title`` / ``source`` / ``source_favicon`` / ``thumbnail`` / ``original_thumbnail`` / ``rating`` / ``reviews`` / ``in_stock``, plus ``price`` (``{value, currency, extracted}``) and the raw ``tag`` chip it is parsed from, on shoppable matches. ``related_searches`` chips come alongside. Legacy ``results`` alias kept for backwards compat.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$url = 'url_example'; // string | Public URL of the image to search visually
$query = 'query_example'; // string | Optional text refinement (e.g. 'pizza')
$country = 'country_example'; // string | ISO country code (alias for gl)
$language = 'language_example'; // string | Language code (alias for hl)
$gl = 'us'; // string | Country code
$hl = 'en'; // string | Language code
$product = false; // bool | Bias towards shoppable product matches
$visual_matches = true; // bool | Include the visual-matches carousel
$exact_matches = false; // bool | Restrict to exact-match results

try {
    $result = $apiInstance->googleGoogleLensVisualSearch($url, $query, $country, $language, $gl, $hl, $product, $visual_matches, $exact_matches);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGoogleLensVisualSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **url** | **string**| Public URL of the image to search visually | |
| **query** | **string**| Optional text refinement (e.g. &#39;pizza&#39;) | [optional] |
| **country** | **string**| ISO country code (alias for gl) | [optional] |
| **language** | **string**| Language code (alias for hl) | [optional] |
| **gl** | **string**| Country code | [optional] [default to &#39;us&#39;] |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **product** | **bool**| Bias towards shoppable product matches | [optional] [default to false] |
| **visual_matches** | **bool**| Include the visual-matches carousel | [optional] [default to true] |
| **exact_matches** | **bool**| Restrict to exact-match results | [optional] [default to false] |

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

## `googleGoogleScraperHealthCheck()`

```php
googleGoogleScraperHealthCheck(): mixed
```

Google scraper health check

Check health of the Google scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->googleGoogleScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGoogleScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `googleGoogleScraperHealthCheckHead()`

```php
googleGoogleScraperHealthCheckHead(): mixed
```

Google scraper health check

Check health of the Google scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->googleGoogleScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGoogleScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `googleGoogleSearchSuggestions()`

```php
googleGoogleSearchSuggestions($q, $hl, $gl): mixed
```

Google search suggestions

Get Google search autocomplete suggestions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query to get suggestions for
$hl = 'en'; // string | Language code
$gl = 'us'; // string | Country code

try {
    $result = $apiInstance->googleGoogleSearchSuggestions($q, $hl, $gl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGoogleSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query to get suggestions for | |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **gl** | **string**| Country code | [optional] [default to &#39;us&#39;] |

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

## `googleGoogleShortsSearch()`

```php
googleGoogleShortsSearch($q, $gl, $hl, $domain, $num, $start): mixed
```

Google Shorts search

Return short-form video results (YouTube Shorts, TikToks) from Google Shorts mode.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query
$gl = 'us'; // string | Country code
$hl = 'en'; // string | Language code
$domain = 'google.com'; // string | Google domain
$num = 20; // int | Results per page
$start = 0; // int | Pagination offset

try {
    $result = $apiInstance->googleGoogleShortsSearch($q, $gl, $hl, $domain, $num, $start);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGoogleShortsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query | |
| **gl** | **string**| Country code | [optional] [default to &#39;us&#39;] |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **domain** | **string**| Google domain | [optional] [default to &#39;google.com&#39;] |
| **num** | **int**| Results per page | [optional] [default to 20] |
| **start** | **int**| Pagination offset | [optional] [default to 0] |

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

## `googleGoogleWebSearch()`

```php
googleGoogleWebSearch($q, $gl, $hl, $num, $start, $domain, $device, $user_agent, $output, $location, $lr, $tbs, $safe, $uule, $filter, $nfpr, $cr, $ludocid, $lsig, $kgmid, $si, $ibp, $uds, $ai_overview): mixed
```

Google web search

Search Google and get structured results (organic, ads, KG, AI overview, PAA).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query (supports Google operators)
$gl = 'us'; // string | Country code
$hl = 'en'; // string | Language code
$num = 10; // int
$start = 0; // int | Page offset (0, 10, 20...)
$domain = 'google.com'; // string | Google domain
$device = 'desktop'; // string | Device target: desktop, mobile, iphone, android, tablet
$user_agent = 'user_agent_example'; // string | Custom User-Agent (overrides device)
$output = 'json'; // string | Response format: json (parsed) or html (raw SERP)
$location = 'location_example'; // string | City-level geo-targeting
$lr = 'lr_example'; // string | Language restrict (e.g. lang_en)
$tbs = 'tbs_example'; // string | Time filter (e.g. qdr:d)
$safe = 'off'; // string
$uule = 'uule_example'; // string | UULE encoded location
$filter = 56; // int | Show omitted results
$nfpr = 0; // int | Disable auto-correction
$cr = 'cr_example'; // string | Country restrict
$ludocid = 'ludocid_example'; // string | Google Place CID
$lsig = 'lsig_example'; // string | Knowledge Graph map ID
$kgmid = 'kgmid_example'; // string | Knowledge Graph entity ID
$si = 'si_example'; // string | Cached search params
$ibp = 'ibp_example'; // string | Layout control
$uds = 'uds_example'; // string | Google filter string
$ai_overview = false; // bool | Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview.

try {
    $result = $apiInstance->googleGoogleWebSearch($q, $gl, $hl, $num, $start, $domain, $device, $user_agent, $output, $location, $lr, $tbs, $safe, $uule, $filter, $nfpr, $cr, $ludocid, $lsig, $kgmid, $si, $ibp, $uds, $ai_overview);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleGoogleWebSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query (supports Google operators) | |
| **gl** | **string**| Country code | [optional] [default to &#39;us&#39;] |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **num** | **int**|  | [optional] [default to 10] |
| **start** | **int**| Page offset (0, 10, 20...) | [optional] [default to 0] |
| **domain** | **string**| Google domain | [optional] [default to &#39;google.com&#39;] |
| **device** | **string**| Device target: desktop, mobile, iphone, android, tablet | [optional] [default to &#39;desktop&#39;] |
| **user_agent** | **string**| Custom User-Agent (overrides device) | [optional] |
| **output** | **string**| Response format: json (parsed) or html (raw SERP) | [optional] [default to &#39;json&#39;] |
| **location** | **string**| City-level geo-targeting | [optional] |
| **lr** | **string**| Language restrict (e.g. lang_en) | [optional] |
| **tbs** | **string**| Time filter (e.g. qdr:d) | [optional] |
| **safe** | **string**|  | [optional] [default to &#39;off&#39;] |
| **uule** | **string**| UULE encoded location | [optional] |
| **filter** | **int**| Show omitted results | [optional] |
| **nfpr** | **int**| Disable auto-correction | [optional] [default to 0] |
| **cr** | **string**| Country restrict | [optional] |
| **ludocid** | **string**| Google Place CID | [optional] |
| **lsig** | **string**| Knowledge Graph map ID | [optional] |
| **kgmid** | **string**| Knowledge Graph entity ID | [optional] |
| **si** | **string**| Cached search params | [optional] |
| **ibp** | **string**| Layout control | [optional] |
| **uds** | **string**| Google filter string | [optional] |
| **ai_overview** | **bool**| Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview. | [optional] [default to false] |

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

## `googleHotelDetails()`

```php
googleHotelDetails($property_token, $check_in, $check_out): mixed
```

Hotel details

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$property_token = 'property_token_example'; // string | Property token
$check_in = 'check_in_example'; // string | YYYY-MM-DD
$check_out = 'check_out_example'; // string | YYYY-MM-DD

try {
    $result = $apiInstance->googleHotelDetails($property_token, $check_in, $check_out);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleHotelDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **property_token** | **string**| Property token | |
| **check_in** | **string**| YYYY-MM-DD | |
| **check_out** | **string**| YYYY-MM-DD | |

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

## `googleImmersiveProductDetail()`

```php
googleImmersiveProductDetail($product_id, $q, $gl, $hl, $catalog_id, $image_docid, $headline_offer_docid, $mid, $include_offers, $include_variants): mixed
```

Immersive product detail

Get deep product details from Google's immersive product page.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 'product_id_example'; // string | Google Shopping ``gpcid`` — the product_id returned on ``/shopping/search`` tiles. Scrapingdog-compatible.
$q = 'q_example'; // string | Original search query that surfaced the product. Required by Google's ``/async/oapv`` RPC.
$gl = 'us'; // string | Country code (ISO 3166 alpha-2)
$hl = 'en'; // string | Language code
$catalog_id = 'catalog_id_example'; // string | Optional ``catalogid`` from the Shopping tile (improves parity).
$image_docid = 'image_docid_example'; // string | Optional ``imageDocid`` for higher-fidelity images.
$headline_offer_docid = 'headline_offer_docid_example'; // string | Optional ``headlineOfferDocid`` to pin the featured seller.
$mid = 'mid_example'; // string | Optional Google Knowledge-Graph ``mid``.
$include_offers = false; // bool | When true, fetch the full merchant-offer list via a secondary RPC (``/async/piu_ps``). Adds ~1 s.
$include_variants = false; // bool | When true, fetch size/colour variants via a secondary RPC (``/async/toy_v``). Adds ~1 s.

try {
    $result = $apiInstance->googleImmersiveProductDetail($product_id, $q, $gl, $hl, $catalog_id, $image_docid, $headline_offer_docid, $mid, $include_offers, $include_variants);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleImmersiveProductDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **string**| Google Shopping &#x60;&#x60;gpcid&#x60;&#x60; — the product_id returned on &#x60;&#x60;/shopping/search&#x60;&#x60; tiles. Scrapingdog-compatible. | |
| **q** | **string**| Original search query that surfaced the product. Required by Google&#39;s &#x60;&#x60;/async/oapv&#x60;&#x60; RPC. | |
| **gl** | **string**| Country code (ISO 3166 alpha-2) | [optional] [default to &#39;us&#39;] |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **catalog_id** | **string**| Optional &#x60;&#x60;catalogid&#x60;&#x60; from the Shopping tile (improves parity). | [optional] |
| **image_docid** | **string**| Optional &#x60;&#x60;imageDocid&#x60;&#x60; for higher-fidelity images. | [optional] |
| **headline_offer_docid** | **string**| Optional &#x60;&#x60;headlineOfferDocid&#x60;&#x60; to pin the featured seller. | [optional] |
| **mid** | **string**| Optional Google Knowledge-Graph &#x60;&#x60;mid&#x60;&#x60;. | [optional] |
| **include_offers** | **bool**| When true, fetch the full merchant-offer list via a secondary RPC (&#x60;&#x60;/async/piu_ps&#x60;&#x60;). Adds ~1 s. | [optional] [default to false] |
| **include_variants** | **bool**| When true, fetch size/colour variants via a secondary RPC (&#x60;&#x60;/async/toy_v&#x60;&#x60;). Adds ~1 s. | [optional] [default to false] |

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

## `googleInterestByRegion()`

```php
googleInterestByRegion($q, $geo): mixed
```

Interest by region

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search term
$geo = ''; // string

try {
    $result = $apiInstance->googleInterestByRegion($q, $geo);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleInterestByRegion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search term | |
| **geo** | **string**|  | [optional] [default to &#39;&#39;] |

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

## `googleInterestOverTime()`

```php
googleInterestOverTime($q, $geo, $date): mixed
```

Interest over time

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search terms
$geo = ''; // string
$date = 'today 12-m'; // string

try {
    $result = $apiInstance->googleInterestOverTime($q, $geo, $date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleInterestOverTime: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search terms | |
| **geo** | **string**|  | [optional] [default to &#39;&#39;] |
| **date** | **string**|  | [optional] [default to &#39;today 12-m&#39;] |

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

## `googleMultiSellerOffersByBarcode()`

```php
googleMultiSellerOffersByBarcode($barcode, $gl, $hl): mixed
```

Multi-seller offers by barcode

Resolve a barcode to a product via Google web search, then return its Google Shopping seller offers (source + price per merchant).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$barcode = 'barcode_example'; // string | Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14
$gl = 'gl_example'; // string | Country code (ISO 3166 alpha-2)
$hl = 'en'; // string | Language code

try {
    $result = $apiInstance->googleMultiSellerOffersByBarcode($barcode, $gl, $hl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleMultiSellerOffersByBarcode: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **barcode** | **string**| Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14 | |
| **gl** | **string**| Country code (ISO 3166 alpha-2) | [optional] |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |

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

## `googleNewsByTopic()`

```php
googleNewsByTopic($topic, $hl, $gl, $max_results): mixed
```

News by topic

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$topic = 'topic_example'; // string | Topic name
$hl = 'en'; // string
$gl = 'US'; // string
$max_results = 10; // int

try {
    $result = $apiInstance->googleNewsByTopic($topic, $hl, $gl, $max_results);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleNewsByTopic: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **topic** | **string**| Topic name | |
| **hl** | **string**|  | [optional] [default to &#39;en&#39;] |
| **gl** | **string**|  | [optional] [default to &#39;US&#39;] |
| **max_results** | **int**|  | [optional] [default to 10] |

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

## `googlePatentDetails()`

```php
googlePatentDetails($patent_id): mixed
```

Patent details

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$patent_id = 'patent_id_example'; // string | Patent number

try {
    $result = $apiInstance->googlePatentDetails($patent_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googlePatentDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **patent_id** | **string**| Patent number | |

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

## `googleRelatedTopicsQueries()`

```php
googleRelatedTopicsQueries($q, $geo): mixed
```

Related topics & queries

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search term
$geo = ''; // string

try {
    $result = $apiInstance->googleRelatedTopicsQueries($q, $geo);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleRelatedTopicsQueries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search term | |
| **geo** | **string**|  | [optional] [default to &#39;&#39;] |

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

## `googleSearchGoogleImages()`

```php
googleSearchGoogleImages($q, $gl, $hl, $tbs, $imgsz, $imgcolor, $imgtype, $safe, $page): mixed
```

Search Google Images

Search Google Images for visual content.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Image search query
$gl = 'us'; // string | Country code
$hl = 'en'; // string | Language code
$tbs = 'tbs_example'; // string | Time/filter string (e.g. qdr:d)
$imgsz = 'imgsz_example'; // string | Image size: l, m, i, xXl
$imgcolor = 'imgcolor_example'; // string | Image color filter
$imgtype = 'imgtype_example'; // string | Image type: face, photo, clipart
$safe = 'off'; // string | Safe search
$page = 0; // int | Page number

try {
    $result = $apiInstance->googleSearchGoogleImages($q, $gl, $hl, $tbs, $imgsz, $imgcolor, $imgtype, $safe, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleSearchGoogleImages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Image search query | |
| **gl** | **string**| Country code | [optional] [default to &#39;us&#39;] |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **tbs** | **string**| Time/filter string (e.g. qdr:d) | [optional] |
| **imgsz** | **string**| Image size: l, m, i, xXl | [optional] |
| **imgcolor** | **string**| Image color filter | [optional] |
| **imgtype** | **string**| Image type: face, photo, clipart | [optional] |
| **safe** | **string**| Safe search | [optional] [default to &#39;off&#39;] |
| **page** | **int**| Page number | [optional] [default to 0] |

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

## `googleSearchGoogleJobs()`

```php
googleSearchGoogleJobs($q, $location, $gl, $job_type, $date_posted): mixed
```

Search Google Jobs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Job title, keywords
$location = 'location_example'; // string
$gl = 'us'; // string
$job_type = 'job_type_example'; // string
$date_posted = 'date_posted_example'; // string

try {
    $result = $apiInstance->googleSearchGoogleJobs($q, $location, $gl, $job_type, $date_posted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleSearchGoogleJobs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Job title, keywords | |
| **location** | **string**|  | [optional] |
| **gl** | **string**|  | [optional] [default to &#39;us&#39;] |
| **job_type** | **string**|  | [optional] |
| **date_posted** | **string**|  | [optional] |

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

## `googleSearchGoogleMapsPlaces()`

```php
googleSearchGoogleMapsPlaces($q, $ll, $gl, $hl, $start): mixed
```

Search Google Maps places

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query
$ll = 'll_example'; // string
$gl = 'us'; // string
$hl = 'en'; // string
$start = 0; // int

try {
    $result = $apiInstance->googleSearchGoogleMapsPlaces($q, $ll, $gl, $hl, $start);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleSearchGoogleMapsPlaces: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query | |
| **ll** | **string**|  | [optional] |
| **gl** | **string**|  | [optional] [default to &#39;us&#39;] |
| **hl** | **string**|  | [optional] [default to &#39;en&#39;] |
| **start** | **int**|  | [optional] [default to 0] |

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

## `googleSearchGoogleNews()`

```php
googleSearchGoogleNews($q, $hl, $gl, $max_results): mixed
```

Search Google News

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query
$hl = 'en'; // string
$gl = 'US'; // string
$max_results = 10; // int

try {
    $result = $apiInstance->googleSearchGoogleNews($q, $hl, $gl, $max_results);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleSearchGoogleNews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query | |
| **hl** | **string**|  | [optional] [default to &#39;en&#39;] |
| **gl** | **string**|  | [optional] [default to &#39;US&#39;] |
| **max_results** | **int**|  | [optional] [default to 10] |

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

## `googleSearchGoogleScholar()`

```php
googleSearchGoogleScholar($q, $hl, $as_ylo, $as_yhi, $as_sdt, $page, $num): mixed
```

Search Google Scholar

Search Google Scholar for scholarly articles.  Each result ships with its doc ``id``, ``type`` badge ([BOOK]/[PDF]/...), wrapped ``inline_links`` (versions + cited_by + related), PDF ``resources`` list, and structured ``authors`` (with ``author_id`` for profiled authors — pipe straight into ``/scholar/author``). Envelope carries ``scholar_results`` alias (Scrapingdog parity), ``related_searches``, and matched ``profiles`` cards.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query for scholarly articles
$hl = 'en'; // string | Language code
$as_ylo = 56; // int | Year from (e.g. 2020)
$as_yhi = 56; // int | Year to (e.g. 2024)
$as_sdt = '0'; // string | Search type: 0=exclude patents, 7=include
$page = 0; // int | Page number (0-based)
$num = 10; // int | Results per page (max 20)

try {
    $result = $apiInstance->googleSearchGoogleScholar($q, $hl, $as_ylo, $as_yhi, $as_sdt, $page, $num);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleSearchGoogleScholar: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query for scholarly articles | |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **as_ylo** | **int**| Year from (e.g. 2020) | [optional] |
| **as_yhi** | **int**| Year to (e.g. 2024) | [optional] |
| **as_sdt** | **string**| Search type: 0&#x3D;exclude patents, 7&#x3D;include | [optional] [default to &#39;0&#39;] |
| **page** | **int**| Page number (0-based) | [optional] [default to 0] |
| **num** | **int**| Results per page (max 20) | [optional] [default to 10] |

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

## `googleSearchGoogleVideos()`

```php
googleSearchGoogleVideos($q, $gl, $hl, $tbs, $safe, $page): mixed
```

Search Google Videos

Search Google for video results.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Video search query
$gl = 'us'; // string | Country code
$hl = 'en'; // string | Language code
$tbs = 'tbs_example'; // string | Time filter (e.g. qdr:d)
$safe = 'off'; // string | Safe search
$page = 0; // int | Page number

try {
    $result = $apiInstance->googleSearchGoogleVideos($q, $gl, $hl, $tbs, $safe, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleSearchGoogleVideos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Video search query | |
| **gl** | **string**| Country code | [optional] [default to &#39;us&#39;] |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **tbs** | **string**| Time filter (e.g. qdr:d) | [optional] |
| **safe** | **string**| Safe search | [optional] [default to &#39;off&#39;] |
| **page** | **int**| Page number | [optional] [default to 0] |

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

## `googleSearchHotels()`

```php
googleSearchHotels($q, $check_in, $check_out, $adults, $currency, $gl): mixed
```

Search hotels

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Location or hotel name
$check_in = 'check_in_example'; // string | YYYY-MM-DD
$check_out = 'check_out_example'; // string | YYYY-MM-DD
$adults = 2; // int
$currency = 'USD'; // string
$gl = 'us'; // string

try {
    $result = $apiInstance->googleSearchHotels($q, $check_in, $check_out, $adults, $currency, $gl);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleSearchHotels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Location or hotel name | |
| **check_in** | **string**| YYYY-MM-DD | |
| **check_out** | **string**| YYYY-MM-DD | |
| **adults** | **int**|  | [optional] [default to 2] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **gl** | **string**|  | [optional] [default to &#39;us&#39;] |

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

## `googleSearchPatents()`

```php
googleSearchPatents($q, $page, $num, $sort, $inventor, $assignee, $country, $language, $status, $patent_type, $before, $after): mixed
```

Search patents

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query (Boolean logic supported)
$page = 0; // int
$num = 10; // int
$sort = 'sort_example'; // string | 'new' or 'old'
$inventor = 'inventor_example'; // string | Inventor name(s)
$assignee = 'assignee_example'; // string | Assignee / company name(s)
$country = 'country_example'; // string | Country code (US, EP, WO, …)
$language = 'language_example'; // string | Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH
$status = 'status_example'; // string | GRANT or APPLICATION
$patent_type = 'patent_type_example'; // string | PATENT or DESIGN
$before = 'before_example'; // string | Before date YYYYMMDD
$after = 'after_example'; // string | After date YYYYMMDD

try {
    $result = $apiInstance->googleSearchPatents($q, $page, $num, $sort, $inventor, $assignee, $country, $language, $status, $patent_type, $before, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleSearchPatents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query (Boolean logic supported) | |
| **page** | **int**|  | [optional] [default to 0] |
| **num** | **int**|  | [optional] [default to 10] |
| **sort** | **string**| &#39;new&#39; or &#39;old&#39; | [optional] |
| **inventor** | **string**| Inventor name(s) | [optional] |
| **assignee** | **string**| Assignee / company name(s) | [optional] |
| **country** | **string**| Country code (US, EP, WO, …) | [optional] |
| **language** | **string**| Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH | [optional] |
| **status** | **string**| GRANT or APPLICATION | [optional] |
| **patent_type** | **string**| PATENT or DESIGN | [optional] |
| **before** | **string**| Before date YYYYMMDD | [optional] |
| **after** | **string**| After date YYYYMMDD | [optional] |

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

## `googleSearchProducts()`

```php
googleSearchProducts($q, $gl, $min_price, $max_price, $sort_by): mixed
```

Search products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Product search query
$gl = 'us'; // string
$min_price = 56; // int
$max_price = 56; // int
$sort_by = 'sort_by_example'; // string

try {
    $result = $apiInstance->googleSearchProducts($q, $gl, $min_price, $max_price, $sort_by);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleSearchProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Product search query | |
| **gl** | **string**|  | [optional] [default to &#39;us&#39;] |
| **min_price** | **int**|  | [optional] |
| **max_price** | **int**|  | [optional] |
| **sort_by** | **string**|  | [optional] |

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

## `googleSearchScholarAuthorProfiles()`

```php
googleSearchScholarAuthorProfiles($mauthors, $hl, $after_author, $before_author): mixed
```

Search Scholar author profiles

Search Google Scholar for author profiles by name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$mauthors = 'mauthors_example'; // string | Author name query (e.g. 'Geoffrey Hinton')
$hl = 'en'; // string | Language code
$after_author = 'after_author_example'; // string | Pagination token (next page)
$before_author = 'before_author_example'; // string | Pagination token (previous page)

try {
    $result = $apiInstance->googleSearchScholarAuthorProfiles($mauthors, $hl, $after_author, $before_author);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleSearchScholarAuthorProfiles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **mauthors** | **string**| Author name query (e.g. &#39;Geoffrey Hinton&#39;) | |
| **hl** | **string**| Language code | [optional] [default to &#39;en&#39;] |
| **after_author** | **string**| Pagination token (next page) | [optional] |
| **before_author** | **string**| Pagination token (previous page) | [optional] |

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

## `googleTrendingNews()`

```php
googleTrendingNews($hl, $gl, $max_results): mixed
```

Trending news

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$hl = 'en'; // string
$gl = 'US'; // string
$max_results = 10; // int

try {
    $result = $apiInstance->googleTrendingNews($hl, $gl, $max_results);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleTrendingNews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **hl** | **string**|  | [optional] [default to &#39;en&#39;] |
| **gl** | **string**|  | [optional] [default to &#39;US&#39;] |
| **max_results** | **int**|  | [optional] [default to 10] |

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

## `googleTrendingSearches()`

```php
googleTrendingSearches($geo): mixed
```

Trending searches

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$geo = 'US'; // string

try {
    $result = $apiInstance->googleTrendingSearches($geo);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleTrendingSearches: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **geo** | **string**|  | [optional] [default to &#39;US&#39;] |

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

## `googleTrendsTopicAutocomplete()`

```php
googleTrendsTopicAutocomplete($q, $hl, $tz): mixed
```

Trends topic autocomplete

Return categorized Knowledge Graph topic entities (mid, type) for a query.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GoogleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Query prefix to resolve into Trends topics
$hl = 'en-US'; // string | Language code
$tz = '0'; // string | Timezone offset in minutes

try {
    $result = $apiInstance->googleTrendsTopicAutocomplete($q, $hl, $tz);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoogleApi->googleTrendsTopicAutocomplete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Query prefix to resolve into Trends topics | |
| **hl** | **string**| Language code | [optional] [default to &#39;en-US&#39;] |
| **tz** | **string**| Timezone offset in minutes | [optional] [default to &#39;0&#39;] |

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

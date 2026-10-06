# ScrapeBadger\NaverApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**naverNaverBlogSearch()**](NaverApi.md#naverNaverBlogSearch) | **GET** /v1/naver/blog | Naver blog search |
| [**naverNaverDatalabShoppingKeywordInsight()**](NaverApi.md#naverNaverDatalabShoppingKeywordInsight) | **GET** /v1/naver/shopping/insight | Naver DataLab shopping keyword insight |
| [**naverNaverNewsSearch()**](NaverApi.md#naverNaverNewsSearch) | **GET** /v1/naver/news | Naver news search |
| [**naverNaverPlaceDetail()**](NaverApi.md#naverNaverPlaceDetail) | **GET** /v1/naver/place/{place_id} | Naver place detail |
| [**naverNaverPlaceLocalSearch()**](NaverApi.md#naverNaverPlaceLocalSearch) | **GET** /v1/naver/local | Naver Place/Local search |
| [**naverNaverPlaceVisitorReviews()**](NaverApi.md#naverNaverPlaceVisitorReviews) | **GET** /v1/naver/place/{place_id}/reviews | Naver place visitor reviews |
| [**naverNaverScraperHealthCheck()**](NaverApi.md#naverNaverScraperHealthCheck) | **GET** /v1/naver/health | Naver scraper health check |
| [**naverNaverScraperHealthCheckHead()**](NaverApi.md#naverNaverScraperHealthCheckHead) | **HEAD** /v1/naver/health | Naver scraper health check |
| [**naverNaverShoppingBestsellerRankings()**](NaverApi.md#naverNaverShoppingBestsellerRankings) | **GET** /v1/naver/shopping/bestsellers | Naver Shopping bestseller rankings |
| [**naverNaverShoppingCategoryReference()**](NaverApi.md#naverNaverShoppingCategoryReference) | **GET** /v1/naver/shopping/categories | Naver Shopping category reference |
| [**naverNaverShoppingTrendingKeywordRankings()**](NaverApi.md#naverNaverShoppingTrendingKeywordRankings) | **GET** /v1/naver/shopping/keywords | Naver Shopping trending keyword rankings |
| [**naverNaverWebSearch()**](NaverApi.md#naverNaverWebSearch) | **GET** /v1/naver/search | Naver web search |
| [**naverSearchSuggestions()**](NaverApi.md#naverSearchSuggestions) | **GET** /v1/naver/autocomplete | Search suggestions |


## `naverNaverBlogSearch()`

```php
naverNaverBlogSearch($query, $page): mixed
```

Naver blog search

Naver blog vertical — post title, blog name and real post URLs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | 검색어
$page = 1; // int

try {
    $result = $apiInstance->naverNaverBlogSearch($query, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverBlogSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| 검색어 | |
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

## `naverNaverDatalabShoppingKeywordInsight()`

```php
naverNaverDatalabShoppingKeywordInsight($category_id, $start_date, $end_date, $time_unit, $count): mixed
```

Naver DataLab shopping keyword insight

DataLab Shopping Insight — top search keywords in a category over a window.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = 'category_id_example'; // string | DataLab category id (cid), e.g. 50000000
$start_date = 'start_date_example'; // string | YYYY-MM-DD
$end_date = 'end_date_example'; // string | YYYY-MM-DD
$time_unit = 'date'; // string | date | week | month
$count = 20; // int | Keywords to return

try {
    $result = $apiInstance->naverNaverDatalabShoppingKeywordInsight($category_id, $start_date, $end_date, $time_unit, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverDatalabShoppingKeywordInsight: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **string**| DataLab category id (cid), e.g. 50000000 | |
| **start_date** | **string**| YYYY-MM-DD | |
| **end_date** | **string**| YYYY-MM-DD | |
| **time_unit** | **string**| date | week | month | [optional] [default to &#39;date&#39;] |
| **count** | **int**| Keywords to return | [optional] [default to 20] |

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

## `naverNaverNewsSearch()`

```php
naverNaverNewsSearch($query, $page): mixed
```

Naver news search

Naver news vertical — publisher, age string and real article URLs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | 검색어
$page = 1; // int

try {
    $result = $apiInstance->naverNaverNewsSearch($query, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverNewsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| 검색어 | |
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

## `naverNaverPlaceDetail()`

```php
naverNaverPlaceDetail($place_id): mixed
```

Naver place detail

Naver Place detail by place id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$place_id = 'place_id_example'; // string

try {
    $result = $apiInstance->naverNaverPlaceDetail($place_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverPlaceDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **place_id** | **string**|  | |

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

## `naverNaverPlaceLocalSearch()`

```php
naverNaverPlaceLocalSearch($query): mixed
```

Naver Place/Local search

Naver Place/Local search — name, category, rating, hours status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Place query, e.g. '성남 카페'

try {
    $result = $apiInstance->naverNaverPlaceLocalSearch($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverPlaceLocalSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Place query, e.g. &#39;성남 카페&#39; | |

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

## `naverNaverPlaceVisitorReviews()`

```php
naverNaverPlaceVisitorReviews($place_id): mixed
```

Naver place visitor reviews

Visitor reviews for a Naver place — rating, body, reviewer, voted keywords, photos.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$place_id = 'place_id_example'; // string

try {
    $result = $apiInstance->naverNaverPlaceVisitorReviews($place_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverPlaceVisitorReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **place_id** | **string**|  | |

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

## `naverNaverScraperHealthCheck()`

```php
naverNaverScraperHealthCheck(): mixed
```

Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->naverNaverScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `naverNaverScraperHealthCheckHead()`

```php
naverNaverScraperHealthCheckHead(): mixed
```

Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->naverNaverScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `naverNaverShoppingBestsellerRankings()`

```php
naverNaverShoppingBestsellerRankings($category_id, $age_type, $sort_type, $period_type): mixed
```

Naver Shopping bestseller rankings

Naver Shopping bestseller rankings — ranked products with price, review score, mall.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = 'ALL'; // string | Naver shopping category id, or ALL
$age_type = 'ALL'; // string | ALL | MEN_20 | WOMEN_20 | ...
$sort_type = 'PRODUCT_CLICK'; // string | PRODUCT_CLICK | PRODUCT_BUY
$period_type = 'DAILY'; // string | DAILY | WEEKLY

try {
    $result = $apiInstance->naverNaverShoppingBestsellerRankings($category_id, $age_type, $sort_type, $period_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverShoppingBestsellerRankings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **string**| Naver shopping category id, or ALL | [optional] [default to &#39;ALL&#39;] |
| **age_type** | **string**| ALL | MEN_20 | WOMEN_20 | ... | [optional] [default to &#39;ALL&#39;] |
| **sort_type** | **string**| PRODUCT_CLICK | PRODUCT_BUY | [optional] [default to &#39;PRODUCT_CLICK&#39;] |
| **period_type** | **string**| DAILY | WEEKLY | [optional] [default to &#39;DAILY&#39;] |

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

## `naverNaverShoppingCategoryReference()`

```php
naverNaverShoppingCategoryReference(): mixed
```

Naver Shopping category reference

Naver Shopping top-level category ids (for bestsellers/keywords/insight). Free.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->naverNaverShoppingCategoryReference();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverShoppingCategoryReference: ', $e->getMessage(), PHP_EOL;
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

## `naverNaverShoppingTrendingKeywordRankings()`

```php
naverNaverShoppingTrendingKeywordRankings($category_id, $age_type, $sort_type, $period_type): mixed
```

Naver Shopping trending keyword rankings

Trending Naver Shopping keywords for a category (snxbest keyword rankings).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = 'category_id_example'; // string | Naver shopping category id (see /shopping/categories)
$age_type = 'ALL'; // string | ALL | MEN_20 | WOMEN_20 | ...
$sort_type = 'KEYWORD_POPULAR'; // string
$period_type = 'WEEKLY'; // string | DAILY | WEEKLY

try {
    $result = $apiInstance->naverNaverShoppingTrendingKeywordRankings($category_id, $age_type, $sort_type, $period_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverShoppingTrendingKeywordRankings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **string**| Naver shopping category id (see /shopping/categories) | |
| **age_type** | **string**| ALL | MEN_20 | WOMEN_20 | ... | [optional] [default to &#39;ALL&#39;] |
| **sort_type** | **string**|  | [optional] [default to &#39;KEYWORD_POPULAR&#39;] |
| **period_type** | **string**| DAILY | WEEKLY | [optional] [default to &#39;WEEKLY&#39;] |

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

## `naverNaverWebSearch()`

```php
naverNaverWebSearch($query, $page): mixed
```

Naver web search

Naver integrated SERP — organic results plus the inline Place pack.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | 검색어, e.g. '성남 카페'
$page = 1; // int | Result page

try {
    $result = $apiInstance->naverNaverWebSearch($query, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverNaverWebSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| 검색어, e.g. &#39;성남 카페&#39; | |
| **page** | **int**| Result page | [optional] [default to 1] |

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

## `naverSearchSuggestions()`

```php
naverSearchSuggestions($query): mixed
```

Search suggestions

Naver search-box suggestions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\NaverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Partial search term

try {
    $result = $apiInstance->naverSearchSuggestions($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NaverApi->naverSearchSuggestions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Partial search term | |

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

# ScrapeBadger\AppStoreApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**appStoreGetAppDetail()**](AppStoreApi.md#appStoreGetAppDetail) | **GET** /v1/app-store/apps/{app_id} | Get app detail |
| [**appStoreGetAppReviews()**](AppStoreApi.md#appStoreGetAppReviews) | **GET** /v1/app-store/apps/{app_id}/reviews | Get app reviews |
| [**appStoreGetDeveloperApps()**](AppStoreApi.md#appStoreGetDeveloperApps) | **GET** /v1/app-store/developers/{artist_id} | Get developer apps |
| [**appStoreListGenres()**](AppStoreApi.md#appStoreListGenres) | **GET** /v1/app-store/genres | List genres |
| [**appStoreListMarkets()**](AppStoreApi.md#appStoreListMarkets) | **GET** /v1/app-store/markets | List markets |
| [**appStoreSearchApps()**](AppStoreApi.md#appStoreSearchApps) | **GET** /v1/app-store/search | Search apps |
| [**appStoreTopCharts()**](AppStoreApi.md#appStoreTopCharts) | **GET** /v1/app-store/charts | Top charts |


## `appStoreGetAppDetail()`

```php
appStoreGetAppDetail($app_id, $country, $lang, $include_extras): mixed
```

Get app detail

App detail: bundle id, version, pricing, ratings, genres, min OS, size, languages, screenshots, in-app purchases and version history.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AppStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | Numeric trackId (e.g. '310633997') or bundle id (e.g. 'net.whatsapp.WhatsApp').
$country = 'us'; // string
$lang = 'lang_example'; // string | Result language, e.g. 'en_us'
$include_extras = true; // bool | Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch.

try {
    $result = $apiInstance->appStoreGetAppDetail($app_id, $country, $lang, $include_extras);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppStoreApi->appStoreGetAppDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| Numeric trackId (e.g. &#39;310633997&#39;) or bundle id (e.g. &#39;net.whatsapp.WhatsApp&#39;). | |
| **country** | **string**|  | [optional] [default to &#39;us&#39;] |
| **lang** | **string**| Result language, e.g. &#39;en_us&#39; | [optional] |
| **include_extras** | **bool**| Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch. | [optional] [default to true] |

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

## `appStoreGetAppReviews()`

```php
appStoreGetAppReviews($app_id, $country, $page, $sort): mixed
```

Get app reviews

Paginated customer reviews (50 per page, up to 10 pages).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AppStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | Numeric trackId, e.g. '310633997'
$country = 'us'; // string
$page = 1; // int | Apple caps reviews at 10 pages
$sort = 'mostRecent'; // string | mostRecent | mostHelpful

try {
    $result = $apiInstance->appStoreGetAppReviews($app_id, $country, $page, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppStoreApi->appStoreGetAppReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| Numeric trackId, e.g. &#39;310633997&#39; | |
| **country** | **string**|  | [optional] [default to &#39;us&#39;] |
| **page** | **int**| Apple caps reviews at 10 pages | [optional] [default to 1] |
| **sort** | **string**| mostRecent | mostHelpful | [optional] [default to &#39;mostRecent&#39;] |

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

## `appStoreGetDeveloperApps()`

```php
appStoreGetDeveloperApps($artist_id, $country): mixed
```

Get developer apps

Developer info and their published apps.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AppStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$artist_id = 'artist_id_example'; // string | Numeric artistId (developer id)
$country = 'us'; // string

try {
    $result = $apiInstance->appStoreGetDeveloperApps($artist_id, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppStoreApi->appStoreGetDeveloperApps: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **artist_id** | **string**| Numeric artistId (developer id) | |
| **country** | **string**|  | [optional] [default to &#39;us&#39;] |

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

## `appStoreListGenres()`

```php
appStoreListGenres(): mixed
```

List genres

The Apple App Store genre/category ids.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AppStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->appStoreListGenres();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppStoreApi->appStoreListGenres: ', $e->getMessage(), PHP_EOL;
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

## `appStoreListMarkets()`

```php
appStoreListMarkets(): mixed
```

List markets

Supported App Store country codes.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AppStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->appStoreListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppStoreApi->appStoreListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `appStoreSearchApps()`

```php
appStoreSearchApps($query, $country, $entity, $limit, $offset, $lang): mixed
```

Search apps

Search the Apple App Store.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AppStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search term, e.g. 'chat'
$country = 'us'; // string | App Store country code
$entity = 'software'; // string | software | iPadSoftware | macSoftware
$limit = 25; // int
$offset = 0; // int
$lang = 'lang_example'; // string | Language, e.g. 'en_us'

try {
    $result = $apiInstance->appStoreSearchApps($query, $country, $entity, $limit, $offset, $lang);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppStoreApi->appStoreSearchApps: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search term, e.g. &#39;chat&#39; | |
| **country** | **string**| App Store country code | [optional] [default to &#39;us&#39;] |
| **entity** | **string**| software | iPadSoftware | macSoftware | [optional] [default to &#39;software&#39;] |
| **limit** | **int**|  | [optional] [default to 25] |
| **offset** | **int**|  | [optional] [default to 0] |
| **lang** | **string**| Language, e.g. &#39;en_us&#39; | [optional] |

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

## `appStoreTopCharts()`

```php
appStoreTopCharts($country, $type, $genre, $limit, $entity): mixed
```

Top charts

Top charts, optionally scoped to a genre.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AppStoreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country = 'us'; // string
$type = 'top-free'; // string | top-free | top-paid | top-grossing
$genre = 56; // int | Apple genre id (optional), e.g. 6014
$limit = 50; // int
$entity = 'apps'; // string | apps (iPhone) | ipad

try {
    $result = $apiInstance->appStoreTopCharts($country, $type, $genre, $limit, $entity);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppStoreApi->appStoreTopCharts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **country** | **string**|  | [optional] [default to &#39;us&#39;] |
| **type** | **string**| top-free | top-paid | top-grossing | [optional] [default to &#39;top-free&#39;] |
| **genre** | **int**| Apple genre id (optional), e.g. 6014 | [optional] |
| **limit** | **int**|  | [optional] [default to 50] |
| **entity** | **string**| apps (iPhone) | ipad | [optional] [default to &#39;apps&#39;] |

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

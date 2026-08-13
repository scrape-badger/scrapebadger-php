# ScrapeBadger\GooglePlayApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**googlePlayBrowseACategory()**](GooglePlayApi.md#googlePlayBrowseACategory) | **GET** /v1/google-play/categories/{category_id} | Browse a category |
| [**googlePlayGetAppDetail()**](GooglePlayApi.md#googlePlayGetAppDetail) | **GET** /v1/google-play/apps/{app_id} | Get app detail |
| [**googlePlayGetAppPermissions()**](GooglePlayApi.md#googlePlayGetAppPermissions) | **GET** /v1/google-play/apps/{app_id}/permissions | Get app permissions |
| [**googlePlayGetAppReviews()**](GooglePlayApi.md#googlePlayGetAppReviews) | **GET** /v1/google-play/apps/{app_id}/reviews | Get app reviews |
| [**googlePlayGetDeveloperApps()**](GooglePlayApi.md#googlePlayGetDeveloperApps) | **GET** /v1/google-play/developers/{developer} | Get developer apps |
| [**googlePlayGetSimilarApps()**](GooglePlayApi.md#googlePlayGetSimilarApps) | **GET** /v1/google-play/apps/{app_id}/similar | Get similar apps |
| [**googlePlayListCategories()**](GooglePlayApi.md#googlePlayListCategories) | **GET** /v1/google-play/categories | List categories |
| [**googlePlayListMarkets()**](GooglePlayApi.md#googlePlayListMarkets) | **GET** /v1/google-play/markets | List markets |
| [**googlePlaySearchApps()**](GooglePlayApi.md#googlePlaySearchApps) | **GET** /v1/google-play/search | Search apps |
| [**googlePlayTopCharts()**](GooglePlayApi.md#googlePlayTopCharts) | **GET** /v1/google-play/collections/{collection} | Top charts |


## `googlePlayBrowseACategory()`

```php
googlePlayBrowseACategory($category_id, $country, $lang, $num): mixed
```

Browse a category

The top apps within a Play category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GooglePlayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category_id = 'category_id_example'; // string | Play category id, e.g. 'GAME_PUZZLE' or 'SOCIAL'
$country = 'US'; // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
$lang = 'en'; // string | Play content language (hl), e.g. 'en' or 'pt-BR'
$num = 100; // int | Max apps; follows each rail's 'see more' continuation above the ~40-120 the page renders directly

try {
    $result = $apiInstance->googlePlayBrowseACategory($category_id, $country, $lang, $num);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GooglePlayApi->googlePlayBrowseACategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category_id** | **string**| Play category id, e.g. &#39;GAME_PUZZLE&#39; or &#39;SOCIAL&#39; | |
| **country** | **string**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &#39;US&#39;] |
| **lang** | **string**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &#39;en&#39;] |
| **num** | **int**| Max apps; follows each rail&#39;s &#39;see more&#39; continuation above the ~40-120 the page renders directly | [optional] [default to 100] |

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

## `googlePlayGetAppDetail()`

```php
googlePlayGetAppDetail($app_id, $country, $lang): mixed
```

Get app detail

Full app detail: ratings histogram, installs, pricing, IAP, developer, screenshots, version metadata and what's-new.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GooglePlayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | Android package id, e.g. 'com.whatsapp'.
$country = 'US'; // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
$lang = 'en'; // string | Play content language (hl), e.g. 'en' or 'pt-BR'

try {
    $result = $apiInstance->googlePlayGetAppDetail($app_id, $country, $lang);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GooglePlayApi->googlePlayGetAppDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| Android package id, e.g. &#39;com.whatsapp&#39;. | |
| **country** | **string**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &#39;US&#39;] |
| **lang** | **string**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &#39;en&#39;] |

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

## `googlePlayGetAppPermissions()`

```php
googlePlayGetAppPermissions($app_id, $lang): mixed
```

Get app permissions

The app's requested Android permissions, grouped.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GooglePlayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | Android package id, e.g. 'com.whatsapp'.
$lang = 'en'; // string | Play content language (hl), e.g. 'en' or 'pt-BR'

try {
    $result = $apiInstance->googlePlayGetAppPermissions($app_id, $lang);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GooglePlayApi->googlePlayGetAppPermissions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| Android package id, e.g. &#39;com.whatsapp&#39;. | |
| **lang** | **string**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &#39;en&#39;] |

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

## `googlePlayGetAppReviews()`

```php
googlePlayGetAppReviews($app_id, $country, $lang, $sort, $count, $page_token): mixed
```

Get app reviews

Paginated app reviews via the Play batchexecute RPC.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GooglePlayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | Android package id, e.g. 'com.whatsapp'.
$country = 'US'; // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
$lang = 'en'; // string | Play content language (hl), e.g. 'en' or 'pt-BR'
$sort = 'newest'; // string | newest | rating | helpfulness
$count = 40; // int
$page_token = 'page_token_example'; // string | Pagination token

try {
    $result = $apiInstance->googlePlayGetAppReviews($app_id, $country, $lang, $sort, $count, $page_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GooglePlayApi->googlePlayGetAppReviews: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| Android package id, e.g. &#39;com.whatsapp&#39;. | |
| **country** | **string**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &#39;US&#39;] |
| **lang** | **string**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &#39;en&#39;] |
| **sort** | **string**| newest | rating | helpfulness | [optional] [default to &#39;newest&#39;] |
| **count** | **int**|  | [optional] [default to 40] |
| **page_token** | **string**| Pagination token | [optional] |

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

## `googlePlayGetDeveloperApps()`

```php
googlePlayGetDeveloperApps($developer, $country, $lang, $num): mixed
```

Get developer apps

A developer's published apps.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GooglePlayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$developer = 'developer_example'; // string | Developer name or numeric id
$country = 'US'; // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
$lang = 'en'; // string | Play content language (hl), e.g. 'en' or 'pt-BR'
$num = 100; // int | Max apps; follows rail continuations above the page's directly-rendered slice

try {
    $result = $apiInstance->googlePlayGetDeveloperApps($developer, $country, $lang, $num);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GooglePlayApi->googlePlayGetDeveloperApps: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **developer** | **string**| Developer name or numeric id | |
| **country** | **string**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &#39;US&#39;] |
| **lang** | **string**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &#39;en&#39;] |
| **num** | **int**| Max apps; follows rail continuations above the page&#39;s directly-rendered slice | [optional] [default to 100] |

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

## `googlePlayGetSimilarApps()`

```php
googlePlayGetSimilarApps($app_id, $country, $lang): mixed
```

Get similar apps

Apps Google Play lists as similar to this one.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GooglePlayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | Android package id, e.g. 'com.whatsapp'.
$country = 'US'; // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
$lang = 'en'; // string | Play content language (hl), e.g. 'en' or 'pt-BR'

try {
    $result = $apiInstance->googlePlayGetSimilarApps($app_id, $country, $lang);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GooglePlayApi->googlePlayGetSimilarApps: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| Android package id, e.g. &#39;com.whatsapp&#39;. | |
| **country** | **string**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &#39;US&#39;] |
| **lang** | **string**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &#39;en&#39;] |

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

## `googlePlayListCategories()`

```php
googlePlayListCategories(): mixed
```

List categories

The Google Play app/game category ids.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GooglePlayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->googlePlayListCategories();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GooglePlayApi->googlePlayListCategories: ', $e->getMessage(), PHP_EOL;
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

## `googlePlayListMarkets()`

```php
googlePlayListMarkets(): mixed
```

List markets

Supported Google Play store countries and languages.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GooglePlayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->googlePlayListMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GooglePlayApi->googlePlayListMarkets: ', $e->getMessage(), PHP_EOL;
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

## `googlePlaySearchApps()`

```php
googlePlaySearchApps($query, $country, $lang, $price): mixed
```

Search apps

Search Google Play for apps and games (the ~30 server-rendered results; Play exposes no page parameter).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GooglePlayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords, e.g. 'puzzle'
$country = 'US'; // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
$lang = 'en'; // string | Play content language (hl), e.g. 'en' or 'pt-BR'
$price = 'price_example'; // string | free | paid | all

try {
    $result = $apiInstance->googlePlaySearchApps($query, $country, $lang, $price);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GooglePlayApi->googlePlaySearchApps: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords, e.g. &#39;puzzle&#39; | |
| **country** | **string**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &#39;US&#39;] |
| **lang** | **string**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &#39;en&#39;] |
| **price** | **string**| free | paid | all | [optional] |

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

## `googlePlayTopCharts()`

```php
googlePlayTopCharts($collection, $category, $country, $lang): mixed
```

Top charts

Top charts for a collection, optionally scoped to a category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GooglePlayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$collection = 'collection_example'; // string | topselling_free | topselling_paid | topgrossing
$category = 'APPLICATION'; // string | Play category, e.g. 'GAME'
$country = 'US'; // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
$lang = 'en'; // string | Play content language (hl), e.g. 'en' or 'pt-BR'

try {
    $result = $apiInstance->googlePlayTopCharts($collection, $category, $country, $lang);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GooglePlayApi->googlePlayTopCharts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **collection** | **string**| topselling_free | topselling_paid | topgrossing | |
| **category** | **string**| Play category, e.g. &#39;GAME&#39; | [optional] [default to &#39;APPLICATION&#39;] |
| **country** | **string**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &#39;US&#39;] |
| **lang** | **string**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &#39;en&#39;] |

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

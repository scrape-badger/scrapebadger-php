# ScrapeBadger\BraveApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**braveAutocomplete()**](BraveApi.md#braveAutocomplete) | **GET** /v1/brave/autocomplete | Autocomplete |
| [**braveImageSearch()**](BraveApi.md#braveImageSearch) | **GET** /v1/brave/images | Image search |
| [**braveListSupportedLocales()**](BraveApi.md#braveListSupportedLocales) | **GET** /v1/brave/locales | List supported locales |
| [**braveNewsSearch()**](BraveApi.md#braveNewsSearch) | **GET** /v1/brave/news | News search |
| [**braveVideoSearch()**](BraveApi.md#braveVideoSearch) | **GET** /v1/brave/videos | Video search |
| [**braveWebSearch()**](BraveApi.md#braveWebSearch) | **GET** /v1/brave/search | Web search |


## `braveAutocomplete()`

```php
braveAutocomplete($query, $country): \ScrapeBadger\Model\BraveAutocompleteResponse
```

Autocomplete

Native search-box suggestions with entity descriptions and images. Two credits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BraveApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string
$country = 'us'; // string

try {
    $result = $apiInstance->braveAutocomplete($query, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BraveApi->braveAutocomplete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**|  | |
| **country** | **string**|  | [optional] [default to &#39;us&#39;] |

### Return type

[**\ScrapeBadger\Model\BraveAutocompleteResponse**](../Model/BraveAutocompleteResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `braveImageSearch()`

```php
braveImageSearch($query, $country, $ui_language, $safe_search, $count): \ScrapeBadger\Model\BraveResponse
```

Image search

Native image batch with original URLs, source pages, thumbnails and dimensions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BraveApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Native Brave search query
$country = 'us'; // string | Native result region; see /locales
$ui_language = 'en-us'; // string | UI labels/date language; does not restrict result language
$safe_search = 'moderate'; // string
$count = 50; // int | Slice the initial native image batch

try {
    $result = $apiInstance->braveImageSearch($query, $country, $ui_language, $safe_search, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BraveApi->braveImageSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Native Brave search query | |
| **country** | **string**| Native result region; see /locales | [optional] [default to &#39;us&#39;] |
| **ui_language** | **string**| UI labels/date language; does not restrict result language | [optional] [default to &#39;en-us&#39;] |
| **safe_search** | **string**|  | [optional] [default to &#39;moderate&#39;] |
| **count** | **int**| Slice the initial native image batch | [optional] [default to 50] |

### Return type

[**\ScrapeBadger\Model\BraveResponse**](../Model/BraveResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `braveListSupportedLocales()`

```php
braveListSupportedLocales(): \ScrapeBadger\Model\BraveLocalesResponse
```

List supported locales

Native country and UI-language choices. Free; result language is a separate preference.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BraveApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->braveListSupportedLocales();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BraveApi->braveListSupportedLocales: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ScrapeBadger\Model\BraveLocalesResponse**](../Model/BraveLocalesResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `braveNewsSearch()`

```php
braveNewsSearch($query, $country, $ui_language, $safe_search, $count): \ScrapeBadger\Model\BraveResponse
```

News search

Native news batch; relative source dates stay display strings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BraveApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Native Brave search query
$country = 'us'; // string | Native result region; see /locales
$ui_language = 'en-us'; // string | UI labels/date language; does not restrict result language
$safe_search = 'moderate'; // string
$count = 35; // int | Slice the initial native news batch

try {
    $result = $apiInstance->braveNewsSearch($query, $country, $ui_language, $safe_search, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BraveApi->braveNewsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Native Brave search query | |
| **country** | **string**| Native result region; see /locales | [optional] [default to &#39;us&#39;] |
| **ui_language** | **string**| UI labels/date language; does not restrict result language | [optional] [default to &#39;en-us&#39;] |
| **safe_search** | **string**|  | [optional] [default to &#39;moderate&#39;] |
| **count** | **int**| Slice the initial native news batch | [optional] [default to 35] |

### Return type

[**\ScrapeBadger\Model\BraveResponse**](../Model/BraveResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `braveVideoSearch()`

```php
braveVideoSearch($query, $country, $ui_language, $safe_search, $page, $count): \ScrapeBadger\Model\BravePagedResponse
```

Video search

Native video results with duration, creator, publisher and verified page ordinals.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BraveApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Native Brave search query
$country = 'us'; // string | Native result region; see /locales
$ui_language = 'en-us'; // string | UI labels/date language; does not restrict result language
$safe_search = 'moderate'; // string
$page = 1; // int | 1-based native page ordinal
$count = 50; // int

try {
    $result = $apiInstance->braveVideoSearch($query, $country, $ui_language, $safe_search, $page, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BraveApi->braveVideoSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Native Brave search query | |
| **country** | **string**| Native result region; see /locales | [optional] [default to &#39;us&#39;] |
| **ui_language** | **string**| UI labels/date language; does not restrict result language | [optional] [default to &#39;en-us&#39;] |
| **safe_search** | **string**|  | [optional] [default to &#39;moderate&#39;] |
| **page** | **int**| 1-based native page ordinal | [optional] [default to 1] |
| **count** | **int**|  | [optional] [default to 50] |

### Return type

[**\ScrapeBadger\Model\BravePagedResponse**](../Model/BravePagedResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `braveWebSearch()`

```php
braveWebSearch($query, $country, $ui_language, $safe_search, $page, $count, $freshness, $spellcheck): \ScrapeBadger\Model\BraveSearchResponse
```

Web search

Native Brave organic results, rich source blocks and page metadata. Seven credits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BraveApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Native Brave search query
$country = 'us'; // string | Native result region; see /locales
$ui_language = 'en-us'; // string | UI labels/date language; does not restrict result language
$safe_search = 'moderate'; // string
$page = 1; // int | 1-based native page ordinal
$count = 20; // int | Slice one native page; does not change native page boundaries
$freshness = 'any'; // string
$spellcheck = false; // bool | Allow native spelling correction

try {
    $result = $apiInstance->braveWebSearch($query, $country, $ui_language, $safe_search, $page, $count, $freshness, $spellcheck);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BraveApi->braveWebSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Native Brave search query | |
| **country** | **string**| Native result region; see /locales | [optional] [default to &#39;us&#39;] |
| **ui_language** | **string**| UI labels/date language; does not restrict result language | [optional] [default to &#39;en-us&#39;] |
| **safe_search** | **string**|  | [optional] [default to &#39;moderate&#39;] |
| **page** | **int**| 1-based native page ordinal | [optional] [default to 1] |
| **count** | **int**| Slice one native page; does not change native page boundaries | [optional] [default to 20] |
| **freshness** | **string**|  | [optional] [default to &#39;any&#39;] |
| **spellcheck** | **bool**| Allow native spelling correction | [optional] [default to false] |

### Return type

[**\ScrapeBadger\Model\BraveSearchResponse**](../Model/BraveSearchResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

# ScrapeBadger\GrokApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**grokAskGrokAQuestion()**](GrokApi.md#grokAskGrokAQuestion) | **GET** /v1/grok/ask | Ask Grok a question |
| [**grokAskGrokAQuestionPost()**](GrokApi.md#grokAskGrokAQuestionPost) | **POST** /v1/grok/ask | Ask Grok a question (POST) |
| [**grokGetAGrokConversation()**](GrokApi.md#grokGetAGrokConversation) | **GET** /v1/grok/conversations/{conversation_id} | Get a Grok conversation |
| [**grokGrokScraperHealthCheck()**](GrokApi.md#grokGrokScraperHealthCheck) | **GET** /v1/grok/health | Grok scraper health check |
| [**grokGrokScraperHealthCheckHead()**](GrokApi.md#grokGrokScraperHealthCheckHead) | **HEAD** /v1/grok/health | Grok scraper health check |
| [**grokListGrokAssistantModes()**](GrokApi.md#grokListGrokAssistantModes) | **GET** /v1/grok/models | List Grok assistant modes |
| [**grokMeasureBrandVisibilityInGrok()**](GrokApi.md#grokMeasureBrandVisibilityInGrok) | **GET** /v1/grok/brand-visibility | Measure brand visibility in Grok |
| [**grokMeasureBrandVisibilityInGrokPost()**](GrokApi.md#grokMeasureBrandVisibilityInGrokPost) | **POST** /v1/grok/brand-visibility | Measure brand visibility in Grok (POST) |


## `grokAskGrokAQuestion()`

```php
grokAskGrokAQuestion($prompt, $conversation_id, $mode, $web_search): mixed
```

Ask Grok a question

Ask the real Grok assistant and get its answer, web sources, and X post references.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GrokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | Prompt to send to Grok (max 4000 characters).
$conversation_id = 'conversation_id_example'; // string | Existing Grok conversation to continue.
$mode = 'auto'; // string | Assistant mode: auto, fast, or expert.
$web_search = 'auto'; // string | Web and X search: auto, force, or off.

try {
    $result = $apiInstance->grokAskGrokAQuestion($prompt, $conversation_id, $mode, $web_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrokApi->grokAskGrokAQuestion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| Prompt to send to Grok (max 4000 characters). | |
| **conversation_id** | **string**| Existing Grok conversation to continue. | [optional] |
| **mode** | **string**| Assistant mode: auto, fast, or expert. | [optional] [default to &#39;auto&#39;] |
| **web_search** | **string**| Web and X search: auto, force, or off. | [optional] [default to &#39;auto&#39;] |

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

## `grokAskGrokAQuestionPost()`

```php
grokAskGrokAQuestionPost(): mixed
```

Ask Grok a question (POST)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GrokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->grokAskGrokAQuestionPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrokApi->grokAskGrokAQuestionPost: ', $e->getMessage(), PHP_EOL;
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

## `grokGetAGrokConversation()`

```php
grokGetAGrokConversation($conversation_id): mixed
```

Get a Grok conversation

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GrokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$conversation_id = 'conversation_id_example'; // string

try {
    $result = $apiInstance->grokGetAGrokConversation($conversation_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrokApi->grokGetAGrokConversation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **conversation_id** | **string**|  | |

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

## `grokGrokScraperHealthCheck()`

```php
grokGrokScraperHealthCheck(): mixed
```

Grok scraper health check

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GrokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->grokGrokScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrokApi->grokGrokScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `grokGrokScraperHealthCheckHead()`

```php
grokGrokScraperHealthCheckHead(): mixed
```

Grok scraper health check

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GrokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->grokGrokScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrokApi->grokGrokScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `grokListGrokAssistantModes()`

```php
grokListGrokAssistantModes(): mixed
```

List Grok assistant modes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GrokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->grokListGrokAssistantModes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrokApi->grokListGrokAssistantModes: ', $e->getMessage(), PHP_EOL;
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

## `grokMeasureBrandVisibilityInGrok()`

```php
grokMeasureBrandVisibilityInGrok($prompt, $brand, $competitors, $brand_domain, $mode, $web_search): mixed
```

Measure brand visibility in Grok

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GrokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | Buyer or category prompt to send to Grok.
$brand = 'brand_example'; // string | Brand name to measure.
$competitors = array('competitors_example'); // string[] | Competitor brand names.
$brand_domain = 'brand_domain_example'; // string | Brand domain for citation rank.
$mode = 'auto'; // string | Assistant mode: auto, fast, or expert.
$web_search = 'force'; // string | Web and X search mode.

try {
    $result = $apiInstance->grokMeasureBrandVisibilityInGrok($prompt, $brand, $competitors, $brand_domain, $mode, $web_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrokApi->grokMeasureBrandVisibilityInGrok: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| Buyer or category prompt to send to Grok. | |
| **brand** | **string**| Brand name to measure. | |
| **competitors** | [**string[]**](../Model/string.md)| Competitor brand names. | [optional] |
| **brand_domain** | **string**| Brand domain for citation rank. | [optional] |
| **mode** | **string**| Assistant mode: auto, fast, or expert. | [optional] [default to &#39;auto&#39;] |
| **web_search** | **string**| Web and X search mode. | [optional] [default to &#39;force&#39;] |

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

## `grokMeasureBrandVisibilityInGrokPost()`

```php
grokMeasureBrandVisibilityInGrokPost(): mixed
```

Measure brand visibility in Grok (POST)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GrokApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->grokMeasureBrandVisibilityInGrokPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrokApi->grokMeasureBrandVisibilityInGrokPost: ', $e->getMessage(), PHP_EOL;
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

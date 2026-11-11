# ScrapeBadger\MetaAiApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**metaAiAskMetaAiAQuestion()**](MetaAiApi.md#metaAiAskMetaAiAQuestion) | **GET** /v1/meta-ai/ask | Ask Meta AI a question |
| [**metaAiAskMetaAiAQuestionPost()**](MetaAiApi.md#metaAiAskMetaAiAQuestionPost) | **POST** /v1/meta-ai/ask | Ask Meta AI a question (POST) |
| [**metaAiListMetaAiAssistantModes()**](MetaAiApi.md#metaAiListMetaAiAssistantModes) | **GET** /v1/meta-ai/models | List Meta AI assistant modes |
| [**metaAiMetaAiScraperHealthCheck()**](MetaAiApi.md#metaAiMetaAiScraperHealthCheck) | **GET** /v1/meta-ai/health | Meta AI scraper health check |
| [**metaAiMetaAiScraperHealthCheckHead()**](MetaAiApi.md#metaAiMetaAiScraperHealthCheckHead) | **HEAD** /v1/meta-ai/health | Meta AI scraper health check |


## `metaAiAskMetaAiAQuestion()`

```php
metaAiAskMetaAiAQuestion($prompt, $country): mixed
```

Ask Meta AI a question

Send a prompt to meta.ai and get the answer (anonymous, no Meta account).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\MetaAiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | The prompt to send to Meta AI (max 4000 characters).
$country = 'country_example'; // string | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.

try {
    $result = $apiInstance->metaAiAskMetaAiAQuestion($prompt, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaAiApi->metaAiAskMetaAiAQuestion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| The prompt to send to Meta AI (max 4000 characters). | |
| **country** | **string**| ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |

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

## `metaAiAskMetaAiAQuestionPost()`

```php
metaAiAskMetaAiAQuestionPost(): mixed
```

Ask Meta AI a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\MetaAiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->metaAiAskMetaAiAQuestionPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaAiApi->metaAiAskMetaAiAQuestionPost: ', $e->getMessage(), PHP_EOL;
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

## `metaAiListMetaAiAssistantModes()`

```php
metaAiListMetaAiAssistantModes($country): mixed
```

List Meta AI assistant modes

Assistant modes meta.ai currently serves to an anonymous visitor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\MetaAiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country = 'country_example'; // string | ISO-3166 alpha-2 egress country.

try {
    $result = $apiInstance->metaAiListMetaAiAssistantModes($country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaAiApi->metaAiListMetaAiAssistantModes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **country** | **string**| ISO-3166 alpha-2 egress country. | [optional] |

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

## `metaAiMetaAiScraperHealthCheck()`

```php
metaAiMetaAiScraperHealthCheck(): mixed
```

Meta AI scraper health check

Check health of the Meta AI scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\MetaAiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->metaAiMetaAiScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaAiApi->metaAiMetaAiScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `metaAiMetaAiScraperHealthCheckHead()`

```php
metaAiMetaAiScraperHealthCheckHead(): mixed
```

Meta AI scraper health check

Check health of the Meta AI scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\MetaAiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->metaAiMetaAiScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaAiApi->metaAiMetaAiScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

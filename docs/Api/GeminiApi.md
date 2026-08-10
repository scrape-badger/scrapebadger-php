# ScrapeBadger\GeminiApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**geminiAskGeminiAQuestion()**](GeminiApi.md#geminiAskGeminiAQuestion) | **GET** /v1/gemini/ask | Ask Gemini a question |
| [**geminiAskGeminiAQuestionPost()**](GeminiApi.md#geminiAskGeminiAQuestionPost) | **POST** /v1/gemini/ask | Ask Gemini a question (POST) |
| [**geminiGeminiScraperHealthCheck()**](GeminiApi.md#geminiGeminiScraperHealthCheck) | **GET** /v1/gemini/health | Gemini scraper health check |
| [**geminiGeminiScraperHealthCheckHead()**](GeminiApi.md#geminiGeminiScraperHealthCheckHead) | **HEAD** /v1/gemini/health | Gemini scraper health check |
| [**geminiMeasureABrandSVisibilityInAGeminiAnswer()**](GeminiApi.md#geminiMeasureABrandSVisibilityInAGeminiAnswer) | **GET** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer |
| [**geminiMeasureABrandSVisibilityInAGeminiAnswerPost()**](GeminiApi.md#geminiMeasureABrandSVisibilityInAGeminiAnswerPost) | **POST** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer (POST) |


## `geminiAskGeminiAQuestion()`

```php
geminiAskGeminiAQuestion($prompt, $country, $web_search): mixed
```

Ask Gemini a question

Send a prompt to Gemini and get the answer plus the web sources it cited.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GeminiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | The prompt to send to Gemini (max 4096 characters).
$country = 'country_example'; // string | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
$web_search = 'auto'; // string | auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened.

try {
    $result = $apiInstance->geminiAskGeminiAQuestion($prompt, $country, $web_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeminiApi->geminiAskGeminiAQuestion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| The prompt to send to Gemini (max 4096 characters). | |
| **country** | **string**| ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |
| **web_search** | **string**| auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). &#x60;web_search_triggered&#x60; in the response always reports what actually happened. | [optional] [default to &#39;auto&#39;] |

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

## `geminiAskGeminiAQuestionPost()`

```php
geminiAskGeminiAQuestionPost(): mixed
```

Ask Gemini a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GeminiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->geminiAskGeminiAQuestionPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeminiApi->geminiAskGeminiAQuestionPost: ', $e->getMessage(), PHP_EOL;
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

## `geminiGeminiScraperHealthCheck()`

```php
geminiGeminiScraperHealthCheck(): mixed
```

Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GeminiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->geminiGeminiScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeminiApi->geminiGeminiScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `geminiGeminiScraperHealthCheckHead()`

```php
geminiGeminiScraperHealthCheckHead(): mixed
```

Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GeminiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->geminiGeminiScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeminiApi->geminiGeminiScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `geminiMeasureABrandSVisibilityInAGeminiAnswer()`

```php
geminiMeasureABrandSVisibilityInAGeminiAnswer($prompt, $brand, $domain, $aliases, $competitors, $country, $web_search): mixed
```

Measure a brand's visibility in a Gemini answer

Ask Gemini, then report whether the brand is mentioned, cited and how prominently.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GeminiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | The prompt to ask Gemini.
$brand = 'brand_example'; // string | Brand name to look for in the answer.
$domain = 'domain_example'; // string | Brand domain, for citation matching.
$aliases = 'aliases_example'; // string | Comma-separated alternative names.
$competitors = 'competitors_example'; // string | Comma-separated competitor names.
$country = 'country_example'; // string | ISO-3166 alpha-2 egress country.
$web_search = 'force'; // string | auto | force | off

try {
    $result = $apiInstance->geminiMeasureABrandSVisibilityInAGeminiAnswer($prompt, $brand, $domain, $aliases, $competitors, $country, $web_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeminiApi->geminiMeasureABrandSVisibilityInAGeminiAnswer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| The prompt to ask Gemini. | |
| **brand** | **string**| Brand name to look for in the answer. | |
| **domain** | **string**| Brand domain, for citation matching. | [optional] |
| **aliases** | **string**| Comma-separated alternative names. | [optional] |
| **competitors** | **string**| Comma-separated competitor names. | [optional] |
| **country** | **string**| ISO-3166 alpha-2 egress country. | [optional] |
| **web_search** | **string**| auto | force | off | [optional] [default to &#39;force&#39;] |

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

## `geminiMeasureABrandSVisibilityInAGeminiAnswerPost()`

```php
geminiMeasureABrandSVisibilityInAGeminiAnswerPost(): mixed
```

Measure a brand's visibility in a Gemini answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GeminiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->geminiMeasureABrandSVisibilityInAGeminiAnswerPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeminiApi->geminiMeasureABrandSVisibilityInAGeminiAnswerPost: ', $e->getMessage(), PHP_EOL;
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

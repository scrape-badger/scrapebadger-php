# ScrapeBadger\PerplexityApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**perplexityAskPerplexityAQuestion()**](PerplexityApi.md#perplexityAskPerplexityAQuestion) | **GET** /v1/perplexity/ask | Ask Perplexity a question |
| [**perplexityAskPerplexityAQuestionPost()**](PerplexityApi.md#perplexityAskPerplexityAQuestionPost) | **POST** /v1/perplexity/ask | Ask Perplexity a question (POST) |
| [**perplexityMeasureABrandSVisibilityInAPerplexityAnswer()**](PerplexityApi.md#perplexityMeasureABrandSVisibilityInAPerplexityAnswer) | **GET** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer |
| [**perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost()**](PerplexityApi.md#perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost) | **POST** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer (POST) |
| [**perplexityPerplexityScraperHealthCheck()**](PerplexityApi.md#perplexityPerplexityScraperHealthCheck) | **GET** /v1/perplexity/health | Perplexity scraper health check |
| [**perplexityPerplexityScraperHealthCheckHead()**](PerplexityApi.md#perplexityPerplexityScraperHealthCheckHead) | **HEAD** /v1/perplexity/health | Perplexity scraper health check |


## `perplexityAskPerplexityAQuestion()`

```php
perplexityAskPerplexityAQuestion($prompt, $country): mixed
```

Ask Perplexity a question

Send a prompt to Perplexity and get the answer plus the web sources it cited.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\PerplexityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | The prompt to send to Perplexity (max 4096 characters).
$country = 'country_example'; // string | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.

try {
    $result = $apiInstance->perplexityAskPerplexityAQuestion($prompt, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PerplexityApi->perplexityAskPerplexityAQuestion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| The prompt to send to Perplexity (max 4096 characters). | |
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

## `perplexityAskPerplexityAQuestionPost()`

```php
perplexityAskPerplexityAQuestionPost(): mixed
```

Ask Perplexity a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\PerplexityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->perplexityAskPerplexityAQuestionPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PerplexityApi->perplexityAskPerplexityAQuestionPost: ', $e->getMessage(), PHP_EOL;
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

## `perplexityMeasureABrandSVisibilityInAPerplexityAnswer()`

```php
perplexityMeasureABrandSVisibilityInAPerplexityAnswer($prompt, $brand, $domain, $aliases, $competitors, $country): mixed
```

Measure a brand's visibility in a Perplexity answer

Ask Perplexity, then report whether the brand is mentioned, cited and how prominently.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\PerplexityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | The prompt to ask Perplexity.
$brand = 'brand_example'; // string | Brand name to look for in the answer.
$domain = 'domain_example'; // string | Brand domain, for citation matching.
$aliases = 'aliases_example'; // string | Comma-separated alternative names.
$competitors = 'competitors_example'; // string | Comma-separated competitor names.
$country = 'country_example'; // string | ISO-3166 alpha-2 egress country.

try {
    $result = $apiInstance->perplexityMeasureABrandSVisibilityInAPerplexityAnswer($prompt, $brand, $domain, $aliases, $competitors, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PerplexityApi->perplexityMeasureABrandSVisibilityInAPerplexityAnswer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| The prompt to ask Perplexity. | |
| **brand** | **string**| Brand name to look for in the answer. | |
| **domain** | **string**| Brand domain, for citation matching. | [optional] |
| **aliases** | **string**| Comma-separated alternative names. | [optional] |
| **competitors** | **string**| Comma-separated competitor names. | [optional] |
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

## `perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost()`

```php
perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost(): mixed
```

Measure a brand's visibility in a Perplexity answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\PerplexityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PerplexityApi->perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost: ', $e->getMessage(), PHP_EOL;
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

## `perplexityPerplexityScraperHealthCheck()`

```php
perplexityPerplexityScraperHealthCheck(): mixed
```

Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\PerplexityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->perplexityPerplexityScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PerplexityApi->perplexityPerplexityScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `perplexityPerplexityScraperHealthCheckHead()`

```php
perplexityPerplexityScraperHealthCheckHead(): mixed
```

Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\PerplexityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->perplexityPerplexityScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PerplexityApi->perplexityPerplexityScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

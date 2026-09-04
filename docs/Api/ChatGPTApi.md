# ScrapeBadger\ChatGPTApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**chatgptAskChatgptAQuestion()**](ChatGPTApi.md#chatgptAskChatgptAQuestion) | **GET** /v1/chatgpt/ask | Ask ChatGPT a question |
| [**chatgptAskChatgptAQuestionPost()**](ChatGPTApi.md#chatgptAskChatgptAQuestionPost) | **POST** /v1/chatgpt/ask | Ask ChatGPT a question (POST) |
| [**chatgptChatgptScraperHealthCheck()**](ChatGPTApi.md#chatgptChatgptScraperHealthCheck) | **GET** /v1/chatgpt/health | ChatGPT scraper health check |
| [**chatgptChatgptScraperHealthCheckHead()**](ChatGPTApi.md#chatgptChatgptScraperHealthCheckHead) | **HEAD** /v1/chatgpt/health | ChatGPT scraper health check |
| [**chatgptListChatgptModels()**](ChatGPTApi.md#chatgptListChatgptModels) | **GET** /v1/chatgpt/models | List ChatGPT models |
| [**chatgptMeasureABrandSVisibilityInAChatgptAnswer()**](ChatGPTApi.md#chatgptMeasureABrandSVisibilityInAChatgptAnswer) | **GET** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer |
| [**chatgptMeasureABrandSVisibilityInAChatgptAnswerPost()**](ChatGPTApi.md#chatgptMeasureABrandSVisibilityInAChatgptAnswerPost) | **POST** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer (POST) |


## `chatgptAskChatgptAQuestion()`

```php
chatgptAskChatgptAQuestion($prompt, $country, $web_search, $image_url): mixed
```

Ask ChatGPT a question

Send a prompt to ChatGPT and get the answer plus the web sources it cited.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ChatGPTApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | The prompt to send to ChatGPT (max 4096 characters).
$country = 'country_example'; // string | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
$web_search = 'auto'; // string | auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened.
$image_url = 'image_url_example'; // string | Public http(s) URL of an image to attach to the prompt. ChatGPT reads it and answers about it. POST also accepts `image_base64`. Exactly one of the two.

try {
    $result = $apiInstance->chatgptAskChatgptAQuestion($prompt, $country, $web_search, $image_url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatGPTApi->chatgptAskChatgptAQuestion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| The prompt to send to ChatGPT (max 4096 characters). | |
| **country** | **string**| ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |
| **web_search** | **string**| auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). &#x60;web_search_triggered&#x60; in the response always reports what actually happened. | [optional] [default to &#39;auto&#39;] |
| **image_url** | **string**| Public http(s) URL of an image to attach to the prompt. ChatGPT reads it and answers about it. POST also accepts &#x60;image_base64&#x60;. Exactly one of the two. | [optional] |

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

## `chatgptAskChatgptAQuestionPost()`

```php
chatgptAskChatgptAQuestionPost(): mixed
```

Ask ChatGPT a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ChatGPTApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->chatgptAskChatgptAQuestionPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatGPTApi->chatgptAskChatgptAQuestionPost: ', $e->getMessage(), PHP_EOL;
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

## `chatgptChatgptScraperHealthCheck()`

```php
chatgptChatgptScraperHealthCheck(): mixed
```

ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ChatGPTApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->chatgptChatgptScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatGPTApi->chatgptChatgptScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `chatgptChatgptScraperHealthCheckHead()`

```php
chatgptChatgptScraperHealthCheckHead(): mixed
```

ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ChatGPTApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->chatgptChatgptScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatGPTApi->chatgptChatgptScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `chatgptListChatgptModels()`

```php
chatgptListChatgptModels($country): mixed
```

List ChatGPT models

Models chatgpt.com currently serves to an anonymous visitor.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ChatGPTApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country = 'country_example'; // string | ISO-3166 alpha-2 egress country.

try {
    $result = $apiInstance->chatgptListChatgptModels($country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatGPTApi->chatgptListChatgptModels: ', $e->getMessage(), PHP_EOL;
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

## `chatgptMeasureABrandSVisibilityInAChatgptAnswer()`

```php
chatgptMeasureABrandSVisibilityInAChatgptAnswer($prompt, $brand, $domain, $aliases, $competitors, $country, $web_search): mixed
```

Measure a brand's visibility in a ChatGPT answer

Ask ChatGPT, then report whether the brand is mentioned, cited and how prominently.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ChatGPTApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | The prompt to ask ChatGPT.
$brand = 'brand_example'; // string | Brand name to look for in the answer.
$domain = 'domain_example'; // string | Brand domain, for citation matching.
$aliases = 'aliases_example'; // string | Comma-separated alternative names.
$competitors = 'competitors_example'; // string | Comma-separated competitor names.
$country = 'country_example'; // string | ISO-3166 alpha-2 egress country.
$web_search = 'force'; // string | auto | force | off

try {
    $result = $apiInstance->chatgptMeasureABrandSVisibilityInAChatgptAnswer($prompt, $brand, $domain, $aliases, $competitors, $country, $web_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatGPTApi->chatgptMeasureABrandSVisibilityInAChatgptAnswer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| The prompt to ask ChatGPT. | |
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

## `chatgptMeasureABrandSVisibilityInAChatgptAnswerPost()`

```php
chatgptMeasureABrandSVisibilityInAChatgptAnswerPost(): mixed
```

Measure a brand's visibility in a ChatGPT answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\ChatGPTApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->chatgptMeasureABrandSVisibilityInAChatgptAnswerPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatGPTApi->chatgptMeasureABrandSVisibilityInAChatgptAnswerPost: ', $e->getMessage(), PHP_EOL;
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

# ScrapeBadger\CopilotApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**copilotAskCopilotAQuestion()**](CopilotApi.md#copilotAskCopilotAQuestion) | **GET** /v1/copilot/ask | Ask Copilot a question |
| [**copilotAskCopilotAQuestionPost()**](CopilotApi.md#copilotAskCopilotAQuestionPost) | **POST** /v1/copilot/ask | Ask Copilot a question (POST) |
| [**copilotCopilotScraperHealthCheck()**](CopilotApi.md#copilotCopilotScraperHealthCheck) | **GET** /v1/copilot/health | Copilot scraper health check |
| [**copilotCopilotScraperHealthCheckHead()**](CopilotApi.md#copilotCopilotScraperHealthCheckHead) | **HEAD** /v1/copilot/health | Copilot scraper health check |
| [**copilotListCopilotMarkets()**](CopilotApi.md#copilotListCopilotMarkets) | **GET** /v1/copilot/markets | List Copilot markets |
| [**copilotMeasureABrandSVisibilityInACopilotAnswer()**](CopilotApi.md#copilotMeasureABrandSVisibilityInACopilotAnswer) | **GET** /v1/copilot/brand-visibility | Measure a brand&#39;s visibility in a Copilot answer |
| [**copilotMeasureABrandSVisibilityInACopilotAnswerPost()**](CopilotApi.md#copilotMeasureABrandSVisibilityInACopilotAnswerPost) | **POST** /v1/copilot/brand-visibility | Measure a brand&#39;s visibility in a Copilot answer (POST) |


## `copilotAskCopilotAQuestion()`

```php
copilotAskCopilotAQuestion($prompt, $country, $market, $strict_country): mixed
```

Ask Copilot a question

Ask Microsoft Copilot (Copilot Search in Bing) and get the answer plus its cited sources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\CopilotApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | The prompt to send to Copilot (max 2000 characters).
$country = 'country_example'; // string | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market.
$market = 'market_example'; // string | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's.
$strict_country = false; // bool | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`.

try {
    $result = $apiInstance->copilotAskCopilotAQuestion($prompt, $country, $market, $strict_country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CopilotApi->copilotAskCopilotAQuestion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| The prompt to send to Copilot (max 2000 characters). | |
| **country** | **string**| ISO-3166 alpha-2 country to ask from, e.g. &#39;JP&#39;, &#39;US&#39;, &#39;GB&#39;. Unless &#x60;market&#x60; is set, Copilot also answers in that country&#39;s market. | [optional] |
| **market** | **string**| Bing market (language-COUNTRY), e.g. &#39;ja-JP&#39;, &#39;en-GB&#39;. Defaults to the country&#39;s. | [optional] |
| **strict_country** | **bool**| Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional] [default to false] |

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

## `copilotAskCopilotAQuestionPost()`

```php
copilotAskCopilotAQuestionPost(): mixed
```

Ask Copilot a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\CopilotApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->copilotAskCopilotAQuestionPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CopilotApi->copilotAskCopilotAQuestionPost: ', $e->getMessage(), PHP_EOL;
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

## `copilotCopilotScraperHealthCheck()`

```php
copilotCopilotScraperHealthCheck(): mixed
```

Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\CopilotApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->copilotCopilotScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CopilotApi->copilotCopilotScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `copilotCopilotScraperHealthCheckHead()`

```php
copilotCopilotScraperHealthCheckHead(): mixed
```

Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\CopilotApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->copilotCopilotScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CopilotApi->copilotCopilotScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `copilotListCopilotMarkets()`

```php
copilotListCopilotMarkets(): mixed
```

List Copilot markets

The Bing markets Copilot can be asked in.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\CopilotApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->copilotListCopilotMarkets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CopilotApi->copilotListCopilotMarkets: ', $e->getMessage(), PHP_EOL;
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

## `copilotMeasureABrandSVisibilityInACopilotAnswer()`

```php
copilotMeasureABrandSVisibilityInACopilotAnswer($prompt, $brand, $domain, $aliases, $competitors, $country, $market, $strict_country): mixed
```

Measure a brand's visibility in a Copilot answer

Ask Copilot, then report whether the brand is mentioned, cited and how prominently.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\CopilotApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$prompt = 'prompt_example'; // string | The prompt to ask Copilot.
$brand = 'brand_example'; // string | Brand name to look for in the answer.
$domain = 'domain_example'; // string | Brand domain, for citation matching.
$aliases = 'aliases_example'; // string | Comma-separated alternative names.
$competitors = 'competitors_example'; // string | Comma-separated competitor names.
$country = 'country_example'; // string | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market.
$market = 'market_example'; // string | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's.
$strict_country = false; // bool | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`.

try {
    $result = $apiInstance->copilotMeasureABrandSVisibilityInACopilotAnswer($prompt, $brand, $domain, $aliases, $competitors, $country, $market, $strict_country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CopilotApi->copilotMeasureABrandSVisibilityInACopilotAnswer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **prompt** | **string**| The prompt to ask Copilot. | |
| **brand** | **string**| Brand name to look for in the answer. | |
| **domain** | **string**| Brand domain, for citation matching. | [optional] |
| **aliases** | **string**| Comma-separated alternative names. | [optional] |
| **competitors** | **string**| Comma-separated competitor names. | [optional] |
| **country** | **string**| ISO-3166 alpha-2 country to ask from, e.g. &#39;JP&#39;, &#39;US&#39;, &#39;GB&#39;. Unless &#x60;market&#x60; is set, Copilot also answers in that country&#39;s market. | [optional] |
| **market** | **string**| Bing market (language-COUNTRY), e.g. &#39;ja-JP&#39;, &#39;en-GB&#39;. Defaults to the country&#39;s. | [optional] |
| **strict_country** | **bool**| Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional] [default to false] |

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

## `copilotMeasureABrandSVisibilityInACopilotAnswerPost()`

```php
copilotMeasureABrandSVisibilityInACopilotAnswerPost(): mixed
```

Measure a brand's visibility in a Copilot answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\CopilotApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->copilotMeasureABrandSVisibilityInACopilotAnswerPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CopilotApi->copilotMeasureABrandSVisibilityInACopilotAnswerPost: ', $e->getMessage(), PHP_EOL;
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

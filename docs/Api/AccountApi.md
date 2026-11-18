# ScrapeBadger\AccountApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**accountGetAccountInfo()**](AccountApi.md#accountGetAccountInfo) | **GET** /v1/account/me | Get account info |
| [**accountGetTheWebhookSigningSecret()**](AccountApi.md#accountGetTheWebhookSigningSecret) | **GET** /v1/account/webhook-secret | Get the webhook signing secret |
| [**accountRotateTheWebhookSigningSecret()**](AccountApi.md#accountRotateTheWebhookSigningSecret) | **POST** /v1/account/webhook-secret/rotate | Rotate the webhook signing secret |
| [**accountWebhookDeliveries()**](AccountApi.md#accountWebhookDeliveries) | **GET** /v1/account/webhook-deliveries | Webhook deliveries |


## `accountGetAccountInfo()`

```php
accountGetAccountInfo(): \ScrapeBadger\Model\AccountInfo
```

Get account info

Get account details for the authenticated API key.  Returns credit balances, tier, rate limit, and subscription details. No credits are deducted for this call.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->accountGetAccountInfo();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGetAccountInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ScrapeBadger\Model\AccountInfo**](../Model/AccountInfo.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `accountGetTheWebhookSigningSecret()`

```php
accountGetTheWebhookSigningSecret(): \ScrapeBadger\Model\WebhookSecret
```

Get the webhook signing secret

The secret that signs this account's async-request webhooks, created on first read. Verify a delivery by comparing ``X-ScrapeBadger-Signature`` with ``sha256=`` + hex HMAC-SHA256(secret, raw body).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->accountGetTheWebhookSigningSecret();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGetTheWebhookSigningSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ScrapeBadger\Model\WebhookSecret**](../Model/WebhookSecret.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `accountRotateTheWebhookSigningSecret()`

```php
accountRotateTheWebhookSigningSecret(): \ScrapeBadger\Model\WebhookSecret
```

Rotate the webhook signing secret

Replace the signing secret. Deliveries that start from now on are signed with the new one; retries of a delivery already under way keep the old one.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->accountRotateTheWebhookSigningSecret();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountRotateTheWebhookSigningSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ScrapeBadger\Model\WebhookSecret**](../Model/WebhookSecret.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `accountWebhookDeliveries()`

```php
accountWebhookDeliveries($limit): \ScrapeBadger\Model\WebhookDeliveries
```

Webhook deliveries

This account's async-request webhook deliveries of the last 24 h, newest first. Free. Needs a full-access API key, like the webhook secret: a trial key gets `403 trial_not_allowed`, a key restricted to some APIs `403 full_access_required`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int | How many deliveries to return (1-200).

try {
    $result = $apiInstance->accountWebhookDeliveries($limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountWebhookDeliveries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**| How many deliveries to return (1-200). | [optional] [default to 50] |

### Return type

[**\ScrapeBadger\Model\WebhookDeliveries**](../Model/WebhookDeliveries.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

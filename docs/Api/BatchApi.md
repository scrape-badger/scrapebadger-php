# ScrapeBadger\BatchApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**batchSubmitABatchOfAsyncRequests()**](BatchApi.md#batchSubmitABatchOfAsyncRequests) | **POST** /v1/batch | Submit a batch of async requests |


## `batchSubmitABatchOfAsyncRequests()`

```php
batchSubmitABatchOfAsyncRequests($batch_request): mixed
```

Submit a batch of async requests

Submit up to 100 GET reads in one call. Each item runs as its own ``Prefer: respond-async`` request under this key, with the same auth, credit check, rate limit and billing as if it were sent alone, and returns a request_id to poll (or a webhook to ``callback_url``). At most 10 items of a batch run at the same time. Submitting is free; each item bills as it runs. Items are checked against the spendable balance first, at the endpoint's base price, so a batch never starts more than the account can pay for.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\BatchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_request = new \ScrapeBadger\Model\BatchRequest(); // \ScrapeBadger\Model\BatchRequest

try {
    $result = $apiInstance->batchSubmitABatchOfAsyncRequests($batch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchApi->batchSubmitABatchOfAsyncRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_request** | [**\ScrapeBadger\Model\BatchRequest**](../Model/BatchRequest.md)|  | |

### Return type

**mixed**

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

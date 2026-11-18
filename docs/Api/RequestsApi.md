# ScrapeBadger\RequestsApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**requestsCallbackStatus()**](RequestsApi.md#requestsCallbackStatus) | **GET** /v1/requests/{request_id}/callback | Callback status |
| [**requestsPollAnAsyncRequest()**](RequestsApi.md#requestsPollAnAsyncRequest) | **GET** /v1/requests/{request_id} | Poll an async request |


## `requestsCallbackStatus()`

```php
requestsCallbackStatus($request_id): \ScrapeBadger\Model\AsyncCallbackStatus
```

Callback status

Webhook delivery state of a call submitted with `X-Callback-URL` / `callback_url`: kept for 24 h. Free. `404 callback_not_found` for a request without a callback, of another account, or older than 24 h.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request_id = 'request_id_example'; // string

try {
    $result = $apiInstance->requestsCallbackStatus($request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RequestsApi->requestsCallbackStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request_id** | **string**|  | |

### Return type

[**\ScrapeBadger\Model\AsyncCallbackStatus**](../Model/AsyncCallbackStatus.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `requestsPollAnAsyncRequest()`

```php
requestsPollAnAsyncRequest($request_id): mixed
```

Poll an async request

Status or final response of a call made with ``Prefer: respond-async``. While it runs: 202. When done: the original status, headers and body.  The final response carries `X-Callback-Status`, `X-Callback-Attempts` and `X-Callback-Error` for a call submitted with a callback; while it runs, the `202` body has a `callback` object. Full delivery state: `GET /v1/requests/{request_id}/callback`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\RequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request_id = 'request_id_example'; // string

try {
    $result = $apiInstance->requestsPollAnAsyncRequest($request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RequestsApi->requestsPollAnAsyncRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request_id** | **string**|  | |

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

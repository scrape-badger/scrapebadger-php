# ScrapeBadger\FeedbackApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**feedbackReportABugOrSendFeedback()**](FeedbackApi.md#feedbackReportABugOrSendFeedback) | **POST** /v1/feedback | Report a bug or send feedback |


## `feedbackReportABugOrSendFeedback()`

```php
feedbackReportABugOrSendFeedback($feedback_request): mixed
```

Report a bug or send feedback

File a bug (wrong/empty result for valid input, misleading error, price mismatch) or feedback (an API or field you needed and couldn't find). Free, never billed. Pass the failing call's X-Request-ID so we can find it.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FeedbackApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$feedback_request = new \ScrapeBadger\Model\FeedbackRequest(); // \ScrapeBadger\Model\FeedbackRequest

try {
    $result = $apiInstance->feedbackReportABugOrSendFeedback($feedback_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FeedbackApi->feedbackReportABugOrSendFeedback: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **feedback_request** | [**\ScrapeBadger\Model\FeedbackRequest**](../Model/FeedbackRequest.md)|  | |

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

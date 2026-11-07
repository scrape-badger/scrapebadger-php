# ScrapeBadger\GitHubApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**githubGetProfile()**](GitHubApi.md#githubGetProfile) | **GET** /v1/github/profiles/{username} | Get profile |
| [**githubGetRepository()**](GitHubApi.md#githubGetRepository) | **GET** /v1/github/repositories/{owner}/{repo} | Get repository |


## `githubGetProfile()`

```php
githubGetProfile($username, $tab, $year, $page, $next_page_token): \ScrapeBadger\Model\GitHubProfileResponse
```

Get profile

Public user or organization profile, pins/popular repositories, README and contributions.  The overview preserves GitHub's public website sections, including organization-specific metadata. Compact displayed counts are approximate and marked with *_approximate. Unavailable or blocked data is an unbilled error, never an empty success.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GitHubApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string
$tab = 'overview'; // string | Profile section; stars is available for users only
$year = 56; // int | Overview only: 1970 through the current UTC year; activity is December or current month
$page = 56; // int | Repositories only: page number, 30 rows per page
$next_page_token = 'next_page_token_example'; // string | Stars only: previous pagination.next_page_token

try {
    $result = $apiInstance->githubGetProfile($username, $tab, $year, $page, $next_page_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GitHubApi->githubGetProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **tab** | **string**| Profile section; stars is available for users only | [optional] [default to &#39;overview&#39;] |
| **year** | **int**| Overview only: 1970 through the current UTC year; activity is December or current month | [optional] |
| **page** | **int**| Repositories only: page number, 30 rows per page | [optional] |
| **next_page_token** | **string**| Stars only: previous pagination.next_page_token | [optional] |

### Return type

[**\ScrapeBadger\Model\GitHubProfileResponse**](../Model/GitHubProfileResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `githubGetRepository()`

```php
githubGetRepository($owner, $repo): \ScrapeBadger\Model\GitHubRepositoryResponse
```

Get repository

Public default-branch repository detail, native README, files and latest commit.  Use owner.login and name from a profile repository summary. Root file and contributor previews are not exhaustive recursive trees or membership lists. No GitHub token, market, ref, search or pagination parameter is accepted.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\GitHubApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owner = 'owner_example'; // string
$repo = 'repo_example'; // string

try {
    $result = $apiInstance->githubGetRepository($owner, $repo);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GitHubApi->githubGetRepository: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **owner** | **string**|  | |
| **repo** | **string**|  | |

### Return type

[**\ScrapeBadger\Model\GitHubRepositoryResponse**](../Model/GitHubRepositoryResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

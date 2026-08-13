# ScrapeBadger\FacebookApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**facebookBrowseAMarketplaceCategory()**](FacebookApi.md#facebookBrowseAMarketplaceCategory) | **GET** /v1/facebook/marketplace/category/{category} | Browse a Marketplace category |
| [**facebookGetAMarketplaceItem()**](FacebookApi.md#facebookGetAMarketplaceItem) | **GET** /v1/facebook/marketplace/item/{item_id} | Get a Marketplace item |
| [**facebookGetAdvertiserPageInfo()**](FacebookApi.md#facebookGetAdvertiserPageInfo) | **GET** /v1/facebook/ads/pages/{page_id} | Get advertiser page info |
| [**facebookGetAnAd()**](FacebookApi.md#facebookGetAnAd) | **GET** /v1/facebook/ads/{ad_archive_id} | Get an ad |
| [**facebookGetGroupDetail()**](FacebookApi.md#facebookGetGroupDetail) | **GET** /v1/facebook/groups/{group_id} | Get group detail |
| [**facebookGetGroupPosts()**](FacebookApi.md#facebookGetGroupPosts) | **GET** /v1/facebook/groups/{group_id}/posts | Get group posts |
| [**facebookGetPageDetail()**](FacebookApi.md#facebookGetPageDetail) | **GET** /v1/facebook/pages/{identifier} | Get page detail |
| [**facebookGetPagePosts()**](FacebookApi.md#facebookGetPagePosts) | **GET** /v1/facebook/pages/{identifier}/posts | Get page posts |
| [**facebookGetPostComments()**](FacebookApi.md#facebookGetPostComments) | **GET** /v1/facebook/posts/{post_id}/comments | Get post comments |
| [**facebookGetPostDetail()**](FacebookApi.md#facebookGetPostDetail) | **GET** /v1/facebook/posts/{post_id} | Get post detail |
| [**facebookGetProfileDetail()**](FacebookApi.md#facebookGetProfileDetail) | **GET** /v1/facebook/profiles/{identifier} | Get profile detail |
| [**facebookGetProfilePosts()**](FacebookApi.md#facebookGetProfilePosts) | **GET** /v1/facebook/profiles/{identifier}/posts | Get profile posts |
| [**facebookListCategories()**](FacebookApi.md#facebookListCategories) | **GET** /v1/facebook/marketplace/categories | List categories |
| [**facebookListLocations()**](FacebookApi.md#facebookListLocations) | **GET** /v1/facebook/marketplace/locations | List locations |
| [**facebookSearchAdvertiserPages()**](FacebookApi.md#facebookSearchAdvertiserPages) | **GET** /v1/facebook/ads/pages/search | Search advertiser pages |
| [**facebookSearchEvents()**](FacebookApi.md#facebookSearchEvents) | **GET** /v1/facebook/search/events | Search events |
| [**facebookSearchEverything()**](FacebookApi.md#facebookSearchEverything) | **GET** /v1/facebook/search | Search everything |
| [**facebookSearchGroups()**](FacebookApi.md#facebookSearchGroups) | **GET** /v1/facebook/search/groups | Search groups |
| [**facebookSearchMarketplace()**](FacebookApi.md#facebookSearchMarketplace) | **GET** /v1/facebook/marketplace/search | Search Marketplace |
| [**facebookSearchPages()**](FacebookApi.md#facebookSearchPages) | **GET** /v1/facebook/search/pages | Search Pages |
| [**facebookSearchPeople()**](FacebookApi.md#facebookSearchPeople) | **GET** /v1/facebook/search/people | Search people |
| [**facebookSearchPlaces()**](FacebookApi.md#facebookSearchPlaces) | **GET** /v1/facebook/search/places | Search places |
| [**facebookSearchPosts()**](FacebookApi.md#facebookSearchPosts) | **GET** /v1/facebook/search/posts | Search posts |
| [**facebookSearchTheAdLibrary()**](FacebookApi.md#facebookSearchTheAdLibrary) | **GET** /v1/facebook/ads/search | Search the Ad Library |


## `facebookBrowseAMarketplaceCategory()`

```php
facebookBrowseAMarketplaceCategory($category, $location, $min_price, $max_price, $sort_by, $after): mixed
```

Browse a Marketplace category

Browse Marketplace listings in a category (vehicles, electronics, ...).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category = 'category_example'; // string
$location = 'nyc'; // string
$min_price = 56; // int
$max_price = 56; // int
$sort_by = 'sort_by_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookBrowseAMarketplaceCategory($category, $location, $min_price, $max_price, $sort_by, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookBrowseAMarketplaceCategory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category** | **string**|  | |
| **location** | **string**|  | [optional] [default to &#39;nyc&#39;] |
| **min_price** | **int**|  | [optional] |
| **max_price** | **int**|  | [optional] |
| **sort_by** | **string**|  | [optional] |
| **after** | **string**|  | [optional] |

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

## `facebookGetAMarketplaceItem()`

```php
facebookGetAMarketplaceItem($item_id): mixed
```

Get a Marketplace item

Get full detail for a single Marketplace listing.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = 'item_id_example'; // string

try {
    $result = $apiInstance->facebookGetAMarketplaceItem($item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetAMarketplaceItem: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **item_id** | **string**|  | |

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

## `facebookGetAdvertiserPageInfo()`

```php
facebookGetAdvertiserPageInfo($page_id, $country): mixed
```

Get advertiser page info

Get advertiser page info: category, followers, page transparency (creation date, name history, managing organization, admin-account locations), related pages, and ad spend (for political/issue advertisers).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_id = 'page_id_example'; // string
$country = 'US'; // string

try {
    $result = $apiInstance->facebookGetAdvertiserPageInfo($page_id, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetAdvertiserPageInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_id** | **string**|  | |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |

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

## `facebookGetAnAd()`

```php
facebookGetAnAd($ad_archive_id, $country): mixed
```

Get an ad

Get a single Ad Library ad by its archive id. For EU/UK-targeted ads the response also includes transparency insights (payer/beneficiary, total EU reach, and age/gender/country reach breakdowns).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ad_archive_id = 'ad_archive_id_example'; // string
$country = 'US'; // string | ISO country code (an EU code returns EU transparency)

try {
    $result = $apiInstance->facebookGetAnAd($ad_archive_id, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetAnAd: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ad_archive_id** | **string**|  | |
| **country** | **string**| ISO country code (an EU code returns EU transparency) | [optional] [default to &#39;US&#39;] |

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

## `facebookGetGroupDetail()`

```php
facebookGetGroupDetail($group_id): mixed
```

Get group detail

Get a Facebook group's details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group_id = 'group_id_example'; // string

try {
    $result = $apiInstance->facebookGetGroupDetail($group_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetGroupDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_id** | **string**|  | |

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

## `facebookGetGroupPosts()`

```php
facebookGetGroupPosts($group_id, $after): mixed
```

Get group posts

Get a Facebook group's post feed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group_id = 'group_id_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookGetGroupPosts($group_id, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetGroupPosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_id** | **string**|  | |
| **after** | **string**|  | [optional] |

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

## `facebookGetPageDetail()`

```php
facebookGetPageDetail($identifier): mixed
```

Get page detail

Get a Facebook Page's profile (name, category, followers, about).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$identifier = 'identifier_example'; // string

try {
    $result = $apiInstance->facebookGetPageDetail($identifier);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetPageDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **identifier** | **string**|  | |

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

## `facebookGetPagePosts()`

```php
facebookGetPagePosts($identifier, $after): mixed
```

Get page posts

Get a Facebook Page's timeline posts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$identifier = 'identifier_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookGetPagePosts($identifier, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetPagePosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **identifier** | **string**|  | |
| **after** | **string**|  | [optional] |

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

## `facebookGetPostComments()`

```php
facebookGetPostComments($post_id, $after, $sort): mixed
```

Get post comments

Get a Facebook post's comment thread (paginated).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_id = 'post_id_example'; // string
$after = 'after_example'; // string
$sort = 'relevance'; // string

try {
    $result = $apiInstance->facebookGetPostComments($post_id, $after, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetPostComments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_id** | **string**|  | |
| **after** | **string**|  | [optional] |
| **sort** | **string**|  | [optional] [default to &#39;relevance&#39;] |

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

## `facebookGetPostDetail()`

```php
facebookGetPostDetail($post_id): mixed
```

Get post detail

Get a Facebook post's detail plus its top comments.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_id = 'post_id_example'; // string

try {
    $result = $apiInstance->facebookGetPostDetail($post_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetPostDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_id** | **string**|  | |

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

## `facebookGetProfileDetail()`

```php
facebookGetProfileDetail($identifier): mixed
```

Get profile detail

Get a Facebook profile's details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$identifier = 'identifier_example'; // string

try {
    $result = $apiInstance->facebookGetProfileDetail($identifier);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetProfileDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **identifier** | **string**|  | |

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

## `facebookGetProfilePosts()`

```php
facebookGetProfilePosts($identifier, $after): mixed
```

Get profile posts

Get a Facebook profile's timeline posts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$identifier = 'identifier_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookGetProfilePosts($identifier, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookGetProfilePosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **identifier** | **string**|  | |
| **after** | **string**|  | [optional] |

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

## `facebookListCategories()`

```php
facebookListCategories(): mixed
```

List categories

List Marketplace category slugs (free).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->facebookListCategories();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookListCategories: ', $e->getMessage(), PHP_EOL;
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

## `facebookListLocations()`

```php
facebookListLocations(): mixed
```

List locations

List common Marketplace location slugs (free).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->facebookListLocations();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookListLocations: ', $e->getMessage(), PHP_EOL;
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

## `facebookSearchAdvertiserPages()`

```php
facebookSearchAdvertiserPages($query, $country): mixed
```

Search advertiser pages

Search advertiser Pages in the Ad Library — returns page ids, categories, likes/followers, verification and Instagram handles.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Advertiser name or keyword
$country = 'US'; // string

try {
    $result = $apiInstance->facebookSearchAdvertiserPages($query, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookSearchAdvertiserPages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Advertiser name or keyword | |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |

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

## `facebookSearchEvents()`

```php
facebookSearchEvents($q, $after): mixed
```

Search events

Search Facebook events.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookSearchEvents($q, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookSearchEvents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**|  | |
| **after** | **string**|  | [optional] |

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

## `facebookSearchEverything()`

```php
facebookSearchEverything($q, $after): mixed
```

Search everything

Global Facebook search (top results across pages, people, groups, posts).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Search query
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookSearchEverything($q, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookSearchEverything: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Search query | |
| **after** | **string**|  | [optional] |

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

## `facebookSearchGroups()`

```php
facebookSearchGroups($q, $after): mixed
```

Search groups

Search Facebook groups.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookSearchGroups($q, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookSearchGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**|  | |
| **after** | **string**|  | [optional] |

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

## `facebookSearchMarketplace()`

```php
facebookSearchMarketplace($query, $location, $min_price, $max_price, $days_since_listed, $sort_by, $item_condition, $delivery_method, $after): mixed
```

Search Marketplace

Search Facebook Marketplace listings by keyword and location.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Search keywords
$location = 'nyc'; // string | Marketplace location slug
$min_price = 56; // int
$max_price = 56; // int
$days_since_listed = 56; // int
$sort_by = 'sort_by_example'; // string
$item_condition = 'item_condition_example'; // string
$delivery_method = 'delivery_method_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookSearchMarketplace($query, $location, $min_price, $max_price, $days_since_listed, $sort_by, $item_condition, $delivery_method, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookSearchMarketplace: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Search keywords | |
| **location** | **string**| Marketplace location slug | [optional] [default to &#39;nyc&#39;] |
| **min_price** | **int**|  | [optional] |
| **max_price** | **int**|  | [optional] |
| **days_since_listed** | **int**|  | [optional] |
| **sort_by** | **string**|  | [optional] |
| **item_condition** | **string**|  | [optional] |
| **delivery_method** | **string**|  | [optional] |
| **after** | **string**|  | [optional] |

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

## `facebookSearchPages()`

```php
facebookSearchPages($q, $after): mixed
```

Search Pages

Search Facebook Pages.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookSearchPages($q, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookSearchPages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**|  | |
| **after** | **string**|  | [optional] |

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

## `facebookSearchPeople()`

```php
facebookSearchPeople($q, $after): mixed
```

Search people

Search Facebook profiles.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookSearchPeople($q, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookSearchPeople: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**|  | |
| **after** | **string**|  | [optional] |

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

## `facebookSearchPlaces()`

```php
facebookSearchPlaces($q, $after): mixed
```

Search places

Search Facebook places.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookSearchPlaces($q, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookSearchPlaces: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**|  | |
| **after** | **string**|  | [optional] |

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

## `facebookSearchPosts()`

```php
facebookSearchPosts($q, $after): mixed
```

Search posts

Search public Facebook posts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookSearchPosts($q, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookSearchPosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**|  | |
| **after** | **string**|  | [optional] |

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

## `facebookSearchTheAdLibrary()`

```php
facebookSearchTheAdLibrary($query, $country, $ad_type, $active_status, $after): mixed
```

Search the Ad Library

Search the Facebook Ad Library.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\FacebookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Advertiser or keyword
$country = 'US'; // string
$ad_type = 'all'; // string
$active_status = 'active'; // string
$after = 'after_example'; // string

try {
    $result = $apiInstance->facebookSearchTheAdLibrary($query, $country, $ad_type, $active_status, $after);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FacebookApi->facebookSearchTheAdLibrary: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Advertiser or keyword | |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **ad_type** | **string**|  | [optional] [default to &#39;all&#39;] |
| **active_status** | **string**|  | [optional] [default to &#39;active&#39;] |
| **after** | **string**|  | [optional] |

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

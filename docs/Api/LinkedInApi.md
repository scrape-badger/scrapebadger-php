# ScrapeBadger\LinkedInApi

All URIs are relative to https://scrapebadger.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**linkedinGetACompanySJobPostings()**](LinkedInApi.md#linkedinGetACompanySJobPostings) | **GET** /v1/linkedin/companies/{company_id}/jobs | Get a company&#39;s job postings |
| [**linkedinGetACourse()**](LinkedInApi.md#linkedinGetACourse) | **GET** /v1/linkedin/learning/{course_slug} | Get a course |
| [**linkedinGetAPublicArticle()**](LinkedInApi.md#linkedinGetAPublicArticle) | **GET** /v1/linkedin/articles/{article_slug} | Get a public article |
| [**linkedinGetAPublicPost()**](LinkedInApi.md#linkedinGetAPublicPost) | **GET** /v1/linkedin/posts/{post_slug} | Get a public post |
| [**linkedinGetCompany()**](LinkedInApi.md#linkedinGetCompany) | **GET** /v1/linkedin/companies/{universal_name} | Get company |
| [**linkedinGetJobDetail()**](LinkedInApi.md#linkedinGetJobDetail) | **GET** /v1/linkedin/jobs/{job_id} | Get job detail |
| [**linkedinGetPublicProfile()**](LinkedInApi.md#linkedinGetPublicProfile) | **GET** /v1/linkedin/profiles/{public_id} | Get public profile |
| [**linkedinGetSchool()**](LinkedInApi.md#linkedinGetSchool) | **GET** /v1/linkedin/schools/{universal_name} | Get school |
| [**linkedinLinkedinScraperHealthCheck()**](LinkedInApi.md#linkedinLinkedinScraperHealthCheck) | **GET** /v1/linkedin/health | LinkedIn scraper health check |
| [**linkedinLinkedinScraperHealthCheckHead()**](LinkedInApi.md#linkedinLinkedinScraperHealthCheckHead) | **HEAD** /v1/linkedin/health | LinkedIn scraper health check |
| [**linkedinSearchLinkedinJobs()**](LinkedInApi.md#linkedinSearchLinkedinJobs) | **GET** /v1/linkedin/jobs/search | Search LinkedIn jobs |
| [**linkedinSuggestLocationGeoIds()**](LinkedInApi.md#linkedinSuggestLocationGeoIds) | **GET** /v1/linkedin/geo/suggest | Suggest location geo ids |


## `linkedinGetACompanySJobPostings()`

```php
linkedinGetACompanySJobPostings($company_id, $start, $country): mixed
```

Get a company's job postings

Public job postings for a company (numeric company id from the company endpoint).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$company_id = 'company_id_example'; // string
$start = 0; // int | Pagination offset (0, 25, 50, ...)
$country = 'us'; // string | Residential proxy country

try {
    $result = $apiInstance->linkedinGetACompanySJobPostings($company_id, $start, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinGetACompanySJobPostings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **company_id** | **string**|  | |
| **start** | **int**| Pagination offset (0, 25, 50, ...) | [optional] [default to 0] |
| **country** | **string**| Residential proxy country | [optional] [default to &#39;us&#39;] |

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

## `linkedinGetACourse()`

```php
linkedinGetACourse($course_slug, $country): mixed
```

Get a course

A public LinkedIn Learning course — provider, workload, instructors, rating.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$course_slug = 'course_slug_example'; // string
$country = 'us'; // string | Residential proxy country

try {
    $result = $apiInstance->linkedinGetACourse($course_slug, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinGetACourse: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **course_slug** | **string**|  | |
| **country** | **string**| Residential proxy country | [optional] [default to &#39;us&#39;] |

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

## `linkedinGetAPublicArticle()`

```php
linkedinGetAPublicArticle($article_slug, $country): mixed
```

Get a public article

A public Pulse article — title, body, author, reactions (JSON-LD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$article_slug = 'article_slug_example'; // string
$country = 'us'; // string | Residential proxy country

try {
    $result = $apiInstance->linkedinGetAPublicArticle($article_slug, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinGetAPublicArticle: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **article_slug** | **string**|  | |
| **country** | **string**| Residential proxy country | [optional] [default to &#39;us&#39;] |

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

## `linkedinGetAPublicPost()`

```php
linkedinGetAPublicPost($post_slug, $country): mixed
```

Get a public post

A public activity share — text, author, reactions, comments (JSON-LD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_slug = 'post_slug_example'; // string
$country = 'us'; // string | Residential proxy country

try {
    $result = $apiInstance->linkedinGetAPublicPost($post_slug, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinGetAPublicPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_slug** | **string**|  | |
| **country** | **string**| Residential proxy country | [optional] [default to &#39;us&#39;] |

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

## `linkedinGetCompany()`

```php
linkedinGetCompany($universal_name, $country): mixed
```

Get company

Public company page — industry, size, HQ, followers, specialties (JSON-LD + SSR).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$universal_name = 'universal_name_example'; // string
$country = 'us'; // string | Residential proxy country

try {
    $result = $apiInstance->linkedinGetCompany($universal_name, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinGetCompany: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **universal_name** | **string**|  | |
| **country** | **string**| Residential proxy country | [optional] [default to &#39;us&#39;] |

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

## `linkedinGetJobDetail()`

```php
linkedinGetJobDetail($job_id, $country): mixed
```

Get job detail

Full detail for one job posting (guest API, no login).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$job_id = 'job_id_example'; // string
$country = 'us'; // string | Residential proxy country

try {
    $result = $apiInstance->linkedinGetJobDetail($job_id, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinGetJobDetail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **job_id** | **string**|  | |
| **country** | **string**| Residential proxy country | [optional] [default to &#39;us&#39;] |

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

## `linkedinGetPublicProfile()`

```php
linkedinGetPublicProfile($public_id, $country): mixed
```

Get public profile

Public profile by vanity id (the ``/in/{public_id}`` slug) — name, headline, location, about, experience, education (public JSON-LD + SSR subset).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$public_id = 'public_id_example'; // string
$country = 'us'; // string | Residential proxy country

try {
    $result = $apiInstance->linkedinGetPublicProfile($public_id, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinGetPublicProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **public_id** | **string**|  | |
| **country** | **string**| Residential proxy country | [optional] [default to &#39;us&#39;] |

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

## `linkedinGetSchool()`

```php
linkedinGetSchool($universal_name, $country): mixed
```

Get school

Public school page — name, description, website, follower/alumni counts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$universal_name = 'universal_name_example'; // string
$country = 'us'; // string | Residential proxy country

try {
    $result = $apiInstance->linkedinGetSchool($universal_name, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinGetSchool: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **universal_name** | **string**|  | |
| **country** | **string**| Residential proxy country | [optional] [default to &#39;us&#39;] |

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

## `linkedinLinkedinScraperHealthCheck()`

```php
linkedinLinkedinScraperHealthCheck(): mixed
```

LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->linkedinLinkedinScraperHealthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinLinkedinScraperHealthCheck: ', $e->getMessage(), PHP_EOL;
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

## `linkedinLinkedinScraperHealthCheckHead()`

```php
linkedinLinkedinScraperHealthCheckHead(): mixed
```

LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->linkedinLinkedinScraperHealthCheckHead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinLinkedinScraperHealthCheckHead: ', $e->getMessage(), PHP_EOL;
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

## `linkedinSearchLinkedinJobs()`

```php
linkedinSearchLinkedinJobs($keywords, $location, $geo_id, $company_id, $date_posted, $experience, $job_type, $workplace, $sort, $start, $country): mixed
```

Search LinkedIn jobs

Search public LinkedIn job postings (guest API, no login).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$keywords = 'keywords_example'; // string | Job title / keywords
$location = 'location_example'; // string | Location text, e.g. 'New York'
$geo_id = 'geo_id_example'; // string | LinkedIn numeric geo id (overrides location)
$company_id = 'company_id_example'; // string | Restrict to a company (numeric id)
$date_posted = 'date_posted_example'; // string | past_24h | past_week | past_month | any
$experience = 'experience_example'; // string | internship|entry|associate|mid_senior|director|executive (comma-separated)
$job_type = 'job_type_example'; // string | full_time|part_time|contract|temporary|internship|volunteer|other
$workplace = 'workplace_example'; // string | onsite|remote|hybrid (comma-separated)
$sort = 'sort_example'; // string | relevant | recent
$start = 0; // int | Pagination offset (0, 25, 50, ...)
$country = 'us'; // string | Residential proxy country

try {
    $result = $apiInstance->linkedinSearchLinkedinJobs($keywords, $location, $geo_id, $company_id, $date_posted, $experience, $job_type, $workplace, $sort, $start, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinSearchLinkedinJobs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **keywords** | **string**| Job title / keywords | [optional] |
| **location** | **string**| Location text, e.g. &#39;New York&#39; | [optional] |
| **geo_id** | **string**| LinkedIn numeric geo id (overrides location) | [optional] |
| **company_id** | **string**| Restrict to a company (numeric id) | [optional] |
| **date_posted** | **string**| past_24h | past_week | past_month | any | [optional] |
| **experience** | **string**| internship|entry|associate|mid_senior|director|executive (comma-separated) | [optional] |
| **job_type** | **string**| full_time|part_time|contract|temporary|internship|volunteer|other | [optional] |
| **workplace** | **string**| onsite|remote|hybrid (comma-separated) | [optional] |
| **sort** | **string**| relevant | recent | [optional] |
| **start** | **int**| Pagination offset (0, 25, 50, ...) | [optional] [default to 0] |
| **country** | **string**| Residential proxy country | [optional] [default to &#39;us&#39;] |

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

## `linkedinSuggestLocationGeoIds()`

```php
linkedinSuggestLocationGeoIds($query, $type): mixed
```

Suggest location geo ids

Resolve a name to LinkedIn ids (job-search ``geo_id`` / ``company_id`` helper).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\LinkedInApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = 'query_example'; // string | Location text, e.g. 'London'
$type = 'geo'; // string | geo | company

try {
    $result = $apiInstance->linkedinSuggestLocationGeoIds($query, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInApi->linkedinSuggestLocationGeoIds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | **string**| Location text, e.g. &#39;London&#39; | |
| **type** | **string**| geo | company | [optional] [default to &#39;geo&#39;] |

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

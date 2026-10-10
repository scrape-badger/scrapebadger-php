# # ExtractRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | The page to fetch. |
**wait_for** | **string** |  | [optional]
**country** | **string** |  | [optional]
**proxy_tier** | **string** | Proxy pool: simple, premium or ultra. | [optional] [default to 'simple']
**extract_rules** | [**array<string,\ScrapeBadger\Model\ExtractRequestExtractRulesValue>**](ExtractRequestExtractRulesValue.md) |  | [optional]
**ai_extract_rules** | **array<string,string>** |  | [optional]
**ai_query** | **string** |  | [optional]
**render_js** | **bool** | Render the page in a browser first. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

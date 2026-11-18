# # WebhookEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | **string** |  |
**request_id** | **string** |  |
**batch_id** | **string** |  |
**status** | **int** | The call&#39;s own HTTP status. |
**headers** | **array<string,string>** | The call&#39;s kept response headers, lower-case (content-type, x-credits-used, x-request-duration-ms, x-api-tier). |
**result_url** | **string** |  |
**result_expires_at** | **int** | Unix time. |
**body_size** | **int** |  |
**body** | **mixed** |  |
**body_omitted** | **bool** | Present (true) when the body was over 1 MB: fetch &#x60;result_url&#x60;. | [optional]
**attempt** | **int** |  |
**sent_at** | **int** | Unix time of this attempt. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

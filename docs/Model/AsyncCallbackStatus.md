# # AsyncCallbackStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**request_id** | **string** |  |
**state** | **string** | &#x60;pending&#x60;: the call is still running. &#x60;delivering&#x60;: an attempt is under way or the next retry is due at &#x60;next_attempt_at&#x60;. &#x60;delivered&#x60;: the endpoint answered 2xx. &#x60;failed&#x60;: every attempt failed, a final status (not 408/429/5xx) came back, or a gateway restart interrupted the delivery (&#x60;last_error&#x60; \&quot;interrupted (gateway restart)\&quot;). |
**attempts** | **int** |  |
**last_status** | **int** |  | [optional]
**last_error** | **string** |  | [optional]
**next_attempt_at** | **int** |  | [optional]
**delivered_at** | **int** |  | [optional]
**callback_host** | **string** | Host of the callback URL only (never its path or query). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

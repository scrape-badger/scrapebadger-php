# # YelpSearchResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**market** | **string** |  |
**query** | **string** |  |
**location** | **string** |  |
**location_resolved** | [**\ScrapeBadger\Model\YelpResolvedLocation**](YelpResolvedLocation.md) |  |
**did_you_mean** | **string** |  | [optional]
**query_matched** | **bool** | False when Yelp could not place the query; results are then Yelp&#39;s broader ranking for the location, as Yelp shows them. |
**total_results** | **int** | Yelp&#39;s reported total; at most 110 are browsable. |
**page** | **int** |  |
**page_size** | **int** |  |
**total_pages** | **int** |  |
**has_next_page** | **bool** |  |
**next_page** | **int** |  | [optional]
**results** | [**\ScrapeBadger\Model\YelpBusiness[]**](YelpBusiness.md) |  |
**ads** | [**\ScrapeBadger\Model\YelpBusiness[]**](YelpBusiness.md) |  |
**filters** | [**array<string,\ScrapeBadger\Model\YelpFilterGroup>**](YelpFilterGroup.md) |  |
**related_searches** | [**\ScrapeBadger\Model\YelpLink[]**](YelpLink.md) |  |
**source_url** | **string** |  |
**fetched_at** | **string** |  |
**fetched_utc** | **float** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

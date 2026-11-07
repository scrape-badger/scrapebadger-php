# # YelpBusiness

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**position** | **int** | 1-based place in Yelp&#39;s organic order across pages (page 2 starts at 11): Yelp&#39;s own number where it numbers the results; services searches are unnumbered and keep Yelp&#39;s order. For ads, the slot order. |
**is_ad** | **bool** |  |
**id** | **string** | Yelp encrypted business ID. |
**alias** | **string** | Business slug used in /biz/&lt;alias&gt;. |
**name** | **string** |  |
**url** | **string** |  |
**rating** | **float** |  | [optional]
**review_count** | **int** |  | [optional]
**price** | **string** |  | [optional]
**price_level** | **int** |  | [optional]
**categories** | [**\ScrapeBadger\Model\YelpCategory[]**](YelpCategory.md) |  | [optional]
**neighborhoods** | **string[]** |  | [optional]
**address** | **string** |  | [optional]
**city** | **string** |  | [optional]
**phone** | **string** |  | [optional]
**timezone** | **string** |  | [optional]
**opening_hours** | [**\ScrapeBadger\Model\YelpHours[]**](YelpHours.md) |  | [optional]
**snippet** | **string** |  | [optional]
**snippet_type** | **string** |  | [optional]
**highlights** | **string[]** |  | [optional]
**tags** | **string[]** |  | [optional]
**photos** | **string[]** |  | [optional]
**alternate_names** | **string[]** |  | [optional]
**is_service_area_business** | **bool** |  | [optional]
**is_yelp_guaranteed** | **bool** |  | [optional]
**has_verified_license** | **bool** |  | [optional]
**ad_placement** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

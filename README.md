<p align="center">
  <img src="https://scrapebadger.com/logo-dark.png" alt="ScrapeBadger" width="400">
</p>

<h1 align="center">ScrapeBadger PHP SDK</h1>

<p align="center">
  <a href="https://packagist.org/packages/scrape-badger/scrapebadger-php"><img src="https://img.shields.io/packagist/v/scrape-badger/scrapebadger-php" alt="version"></a>
  <a href="https://github.com/scrape-badger/scrapebadger-php/actions"><img src="https://img.shields.io/github/actions/workflow/status/scrape-badger/scrapebadger-php/ci.yml?label=CI" alt="CI"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="license"></a>
</p>

Official **PHP** SDK for [ScrapeBadger](https://scrapebadger.com) — one API key for
30+ scraping APIs: Twitter/X, Reddit, Facebook, Instagram, TikTok, YouTube, Amazon, eBay,
Walmart, Vinted, Google (18 products), Bing, Yahoo, ChatGPT, Perplexity, real estate, and
any URL via the general Web Scraping API. Generated from the ScrapeBadger OpenAPI spec —
always in sync with the API. ⚠️ This repository is regenerated automatically; don't send
PRs here, request changes via the [roadmap](https://github.com/scrape-badger/roadmap).

📚 [API docs](https://docs.scrapebadger.com) · 🧰 [All SDKs](https://scrapebadger.com/sdks) · 🔑 [Get an API key](https://scrapebadger.com/auth/signup) — 1,000 free credits

## 🚀 Install

```
composer require scrape-badger/scrapebadger-php
```

## ⚡ Quick start

```php
<?php
require_once __DIR__ . '/vendor/autoload.php';

$config = ScrapeBadger\Configuration::getDefaultConfiguration()
    ->setApiKey('X-API-Key', 'YOUR_API_KEY');

$twitter = new ScrapeBadger\Api\TwitterApi(config: $config);
$user = $twitter->twitterGetUserByUsername('elonmusk');
var_dump($user);
```

Every scraper is available as its own API class (`TwitterApi`, `AmazonApi`, `GoogleApi`, …)
with one method per endpoint — the full list is in the reference below.

## 🛠 Development

```sh
composer install                     # deps
composer validate --strict           # manifest lint
find lib -name '*.php' | xargs -n1 php -l   # syntax
./vendor/bin/phpunit                 # tests
```

---

# OpenAPIClient-php

Unified credit-based scraping API. https://docs.scrapebadger.com


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/scrape-badger/scrapebadger-php.git"
    }
  ],
  "require": {
    "scrape-badger/scrapebadger-php": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: ApiKeyAuth
$config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ScrapeBadger\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new ScrapeBadger\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->accountGetAccountInfo();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGetAccountInfo: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://scrapebadger.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountApi* | [**accountGetAccountInfo**](docs/Api/AccountApi.md#accountgetaccountinfo) | **GET** /v1/account/me | Get account info
*AirbnbApi* | [**airbnbAirbnbScraperHealthCheck**](docs/Api/AirbnbApi.md#airbnbairbnbscraperhealthcheck) | **GET** /v1/airbnb/health | Airbnb scraper health check
*AirbnbApi* | [**airbnbAirbnbScraperHealthCheckHead**](docs/Api/AirbnbApi.md#airbnbairbnbscraperhealthcheckhead) | **HEAD** /v1/airbnb/health | Airbnb scraper health check
*AirbnbApi* | [**airbnbGetAvailabilityCalendar**](docs/Api/AirbnbApi.md#airbnbgetavailabilitycalendar) | **GET** /v1/airbnb/listings/{room_id}/calendar | Get availability calendar
*AirbnbApi* | [**airbnbGetExperienceDetail**](docs/Api/AirbnbApi.md#airbnbgetexperiencedetail) | **GET** /v1/airbnb/experiences/{experience_id} | Get experience detail
*AirbnbApi* | [**airbnbGetListingDetail**](docs/Api/AirbnbApi.md#airbnbgetlistingdetail) | **GET** /v1/airbnb/listings/{room_id} | Get listing detail
*AirbnbApi* | [**airbnbGetListingReviews**](docs/Api/AirbnbApi.md#airbnbgetlistingreviews) | **GET** /v1/airbnb/listings/{room_id}/reviews | Get listing reviews
*AirbnbApi* | [**airbnbSearchExperiences**](docs/Api/AirbnbApi.md#airbnbsearchexperiences) | **GET** /v1/airbnb/experiences | Search experiences
*AirbnbApi* | [**airbnbSearchStays**](docs/Api/AirbnbApi.md#airbnbsearchstays) | **GET** /v1/airbnb/search | Search stays
*AmazonApi* | [**amazonAmazonScraperHealthCheck**](docs/Api/AmazonApi.md#amazonamazonscraperhealthcheck) | **GET** /v1/amazon/health | Amazon scraper health check
*AmazonApi* | [**amazonAmazonScraperHealthCheckHead**](docs/Api/AmazonApi.md#amazonamazonscraperhealthcheckhead) | **HEAD** /v1/amazon/health | Amazon scraper health check
*AmazonApi* | [**amazonBestsellersByCategory**](docs/Api/AmazonApi.md#amazonbestsellersbycategory) | **GET** /v1/amazon/bestsellers | Bestsellers by category
*AmazonApi* | [**amazonBrowseNodeCategoryListing**](docs/Api/AmazonApi.md#amazonbrowsenodecategorylisting) | **GET** /v1/amazon/category | Browse-node category listing
*AmazonApi* | [**amazonGetAllSellerOffersBuybox**](docs/Api/AmazonApi.md#amazongetallselleroffersbuybox) | **GET** /v1/amazon/products/{asin}/offers | Get all seller offers (buybox)
*AmazonApi* | [**amazonGetProductDetail**](docs/Api/AmazonApi.md#amazongetproductdetail) | **GET** /v1/amazon/products/{asin} | Get product detail
*AmazonApi* | [**amazonGetProductReviews**](docs/Api/AmazonApi.md#amazongetproductreviews) | **GET** /v1/amazon/products/{asin}/reviews | Get product reviews
*AmazonApi* | [**amazonGetSellerFeedback**](docs/Api/AmazonApi.md#amazongetsellerfeedback) | **GET** /v1/amazon/sellers/{seller_id}/feedback | Get seller feedback
*AmazonApi* | [**amazonGetSellerProfile**](docs/Api/AmazonApi.md#amazongetsellerprofile) | **GET** /v1/amazon/sellers/{seller_id} | Get seller profile
*AmazonApi* | [**amazonGetSellerStorefrontProducts**](docs/Api/AmazonApi.md#amazongetsellerstorefrontproducts) | **GET** /v1/amazon/sellers/{seller_id}/products | Get seller storefront products
*AmazonApi* | [**amazonKeywordSuggestions**](docs/Api/AmazonApi.md#amazonkeywordsuggestions) | **GET** /v1/amazon/autocomplete | Keyword suggestions
*AmazonApi* | [**amazonListCategoryAliases**](docs/Api/AmazonApi.md#amazonlistcategoryaliases) | **GET** /v1/amazon/categories | List category aliases
*AmazonApi* | [**amazonListMarketplaces**](docs/Api/AmazonApi.md#amazonlistmarketplaces) | **GET** /v1/amazon/markets | List marketplaces
*AmazonApi* | [**amazonNewReleasesByCategory**](docs/Api/AmazonApi.md#amazonnewreleasesbycategory) | **GET** /v1/amazon/new-releases | New releases by category
*AmazonApi* | [**amazonSearchAmazonProducts**](docs/Api/AmazonApi.md#amazonsearchamazonproducts) | **GET** /v1/amazon/search | Search Amazon products
*AmazonApi* | [**amazonTodaySDeals**](docs/Api/AmazonApi.md#amazontodaysdeals) | **GET** /v1/amazon/deals | Today&#39;s deals
*ApartmentsApi* | [**apartmentsApartmentsScraperHealthCheck**](docs/Api/ApartmentsApi.md#apartmentsapartmentsscraperhealthcheck) | **GET** /v1/apartments/health | Apartments scraper health check
*ApartmentsApi* | [**apartmentsApartmentsScraperHealthCheckHead**](docs/Api/ApartmentsApi.md#apartmentsapartmentsscraperhealthcheckhead) | **HEAD** /v1/apartments/health | Apartments scraper health check
*ApartmentsApi* | [**apartmentsGetPropertyDetailBySlugId**](docs/Api/ApartmentsApi.md#apartmentsgetpropertydetailbyslugid) | **GET** /v1/apartments/properties/{slug}/{property_id} | Get property detail by slug + id
*ApartmentsApi* | [**apartmentsGetPropertyDetailByUrl**](docs/Api/ApartmentsApi.md#apartmentsgetpropertydetailbyurl) | **GET** /v1/apartments/property | Get property detail by URL
*ApartmentsApi* | [**apartmentsSearchRentalListings**](docs/Api/ApartmentsApi.md#apartmentssearchrentallistings) | **GET** /v1/apartments/search | Search rental listings
*AppStoreApi* | [**appStoreGetAppDetail**](docs/Api/AppStoreApi.md#appstoregetappdetail) | **GET** /v1/app-store/apps/{app_id} | Get app detail
*AppStoreApi* | [**appStoreGetAppReviews**](docs/Api/AppStoreApi.md#appstoregetappreviews) | **GET** /v1/app-store/apps/{app_id}/reviews | Get app reviews
*AppStoreApi* | [**appStoreGetDeveloperApps**](docs/Api/AppStoreApi.md#appstoregetdeveloperapps) | **GET** /v1/app-store/developers/{artist_id} | Get developer apps
*AppStoreApi* | [**appStoreListGenres**](docs/Api/AppStoreApi.md#appstorelistgenres) | **GET** /v1/app-store/genres | List genres
*AppStoreApi* | [**appStoreListMarkets**](docs/Api/AppStoreApi.md#appstorelistmarkets) | **GET** /v1/app-store/markets | List markets
*AppStoreApi* | [**appStoreSearchApps**](docs/Api/AppStoreApi.md#appstoresearchapps) | **GET** /v1/app-store/search | Search apps
*AppStoreApi* | [**appStoreTopCharts**](docs/Api/AppStoreApi.md#appstoretopcharts) | **GET** /v1/app-store/charts | Top charts
*BaiduApi* | [**baiduBaiduImageSearch**](docs/Api/BaiduApi.md#baidubaiduimagesearch) | **GET** /v1/baidu/images | Baidu image search
*BaiduApi* | [**baiduBaiduNewsSearch**](docs/Api/BaiduApi.md#baidubaidunewssearch) | **GET** /v1/baidu/news | Baidu news search
*BaiduApi* | [**baiduBaiduScraperHealthCheck**](docs/Api/BaiduApi.md#baidubaiduscraperhealthcheck) | **GET** /v1/baidu/health | Baidu scraper health check
*BaiduApi* | [**baiduBaiduScraperHealthCheckHead**](docs/Api/BaiduApi.md#baidubaiduscraperhealthcheckhead) | **HEAD** /v1/baidu/health | Baidu scraper health check
*BaiduApi* | [**baiduBaiduWebSearch**](docs/Api/BaiduApi.md#baidubaiduwebsearch) | **GET** /v1/baidu/search | Baidu web search
*BaiduApi* | [**baiduSearchSuggestions**](docs/Api/BaiduApi.md#baidusearchsuggestions) | **GET** /v1/baidu/autocomplete | Search suggestions
*BingApi* | [**bingBingScraperHealthCheck**](docs/Api/BingApi.md#bingbingscraperhealthcheck) | **GET** /v1/bing/health | Bing scraper health check
*BingApi* | [**bingBingScraperHealthCheckHead**](docs/Api/BingApi.md#bingbingscraperhealthcheckhead) | **HEAD** /v1/bing/health | Bing scraper health check
*BingApi* | [**bingImageSearch**](docs/Api/BingApi.md#bingimagesearch) | **GET** /v1/bing/images | Image search
*BingApi* | [**bingListSupportedMarkets**](docs/Api/BingApi.md#binglistsupportedmarkets) | **GET** /v1/bing/markets | List supported markets
*BingApi* | [**bingNewsSearch**](docs/Api/BingApi.md#bingnewssearch) | **GET** /v1/bing/news | News search
*BingApi* | [**bingSearchSuggestions**](docs/Api/BingApi.md#bingsearchsuggestions) | **GET** /v1/bing/autocomplete | Search suggestions
*BingApi* | [**bingVideoSearch**](docs/Api/BingApi.md#bingvideosearch) | **GET** /v1/bing/videos | Video search
*BingApi* | [**bingWebSearch**](docs/Api/BingApi.md#bingwebsearch) | **GET** /v1/bing/search | Web search
*BookingApi* | [**bookingBookingScraperHealthCheck**](docs/Api/BookingApi.md#bookingbookingscraperhealthcheck) | **GET** /v1/booking/health | Booking scraper health check
*BookingApi* | [**bookingBookingScraperHealthCheckHead**](docs/Api/BookingApi.md#bookingbookingscraperhealthcheckhead) | **HEAD** /v1/booking/health | Booking scraper health check
*BookingApi* | [**bookingGetPropertyDetail**](docs/Api/BookingApi.md#bookinggetpropertydetail) | **GET** /v1/booking/properties/{country_code}/{slug} | Get property detail
*BookingApi* | [**bookingGetPropertyReviews**](docs/Api/BookingApi.md#bookinggetpropertyreviews) | **GET** /v1/booking/properties/{country_code}/{slug}/reviews | Get property reviews
*BookingApi* | [**bookingGetRoomTypesAndLiveRates**](docs/Api/BookingApi.md#bookinggetroomtypesandliverates) | **GET** /v1/booking/properties/{country_code}/{slug}/rooms | Get room types and live rates
*BookingApi* | [**bookingSearchDestinations**](docs/Api/BookingApi.md#bookingsearchdestinations) | **GET** /v1/booking/destinations | Search destinations
*BookingApi* | [**bookingSearchProperties**](docs/Api/BookingApi.md#bookingsearchproperties) | **GET** /v1/booking/search | Search properties
*ChatGPTApi* | [**chatgptAskChatgptAQuestion**](docs/Api/ChatGPTApi.md#chatgptaskchatgptaquestion) | **GET** /v1/chatgpt/ask | Ask ChatGPT a question
*ChatGPTApi* | [**chatgptAskChatgptAQuestionPost**](docs/Api/ChatGPTApi.md#chatgptaskchatgptaquestionpost) | **POST** /v1/chatgpt/ask | Ask ChatGPT a question (POST)
*ChatGPTApi* | [**chatgptChatgptScraperHealthCheck**](docs/Api/ChatGPTApi.md#chatgptchatgptscraperhealthcheck) | **GET** /v1/chatgpt/health | ChatGPT scraper health check
*ChatGPTApi* | [**chatgptChatgptScraperHealthCheckHead**](docs/Api/ChatGPTApi.md#chatgptchatgptscraperhealthcheckhead) | **HEAD** /v1/chatgpt/health | ChatGPT scraper health check
*ChatGPTApi* | [**chatgptListChatgptModels**](docs/Api/ChatGPTApi.md#chatgptlistchatgptmodels) | **GET** /v1/chatgpt/models | List ChatGPT models
*ChatGPTApi* | [**chatgptMeasureABrandSVisibilityInAChatgptAnswer**](docs/Api/ChatGPTApi.md#chatgptmeasureabrandsvisibilityinachatgptanswer) | **GET** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer
*ChatGPTApi* | [**chatgptMeasureABrandSVisibilityInAChatgptAnswerPost**](docs/Api/ChatGPTApi.md#chatgptmeasureabrandsvisibilityinachatgptanswerpost) | **POST** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer (POST)
*DepopApi* | [**depopDepopScraperHealthCheck**](docs/Api/DepopApi.md#depopdepopscraperhealthcheck) | **GET** /v1/depop/health | Depop scraper health check
*DepopApi* | [**depopDepopScraperHealthCheckHead**](docs/Api/DepopApi.md#depopdepopscraperhealthcheckhead) | **HEAD** /v1/depop/health | Depop scraper health check
*DepopApi* | [**depopGetAUserSProducts**](docs/Api/DepopApi.md#depopgetausersproducts) | **GET** /v1/depop/users/{username}/products | Get a user&#39;s products
*DepopApi* | [**depopGetProductDetail**](docs/Api/DepopApi.md#depopgetproductdetail) | **GET** /v1/depop/products/{product_id} | Get product detail
*DepopApi* | [**depopGetShopUserProfile**](docs/Api/DepopApi.md#depopgetshopuserprofile) | **GET** /v1/depop/users/{username} | Get shop/user profile
*DepopApi* | [**depopListMarkets**](docs/Api/DepopApi.md#depoplistmarkets) | **GET** /v1/depop/markets | List markets
*DepopApi* | [**depopSearchDepopProducts**](docs/Api/DepopApi.md#depopsearchdepopproducts) | **GET** /v1/depop/search | Search Depop products
*DuckDuckGoApi* | [**duckduckgoDuckduckgoScraperHealthCheck**](docs/Api/DuckDuckGoApi.md#duckduckgoduckduckgoscraperhealthcheck) | **GET** /v1/duckduckgo/health | DuckDuckGo scraper health check
*DuckDuckGoApi* | [**duckduckgoDuckduckgoScraperHealthCheckHead**](docs/Api/DuckDuckGoApi.md#duckduckgoduckduckgoscraperhealthcheckhead) | **HEAD** /v1/duckduckgo/health | DuckDuckGo scraper health check
*DuckDuckGoApi* | [**duckduckgoImageSearch**](docs/Api/DuckDuckGoApi.md#duckduckgoimagesearch) | **GET** /v1/duckduckgo/images | Image search
*DuckDuckGoApi* | [**duckduckgoInstantAnswer**](docs/Api/DuckDuckGoApi.md#duckduckgoinstantanswer) | **GET** /v1/duckduckgo/instant | Instant Answer
*DuckDuckGoApi* | [**duckduckgoListSupportedRegions**](docs/Api/DuckDuckGoApi.md#duckduckgolistsupportedregions) | **GET** /v1/duckduckgo/regions | List supported regions
*DuckDuckGoApi* | [**duckduckgoNewsSearch**](docs/Api/DuckDuckGoApi.md#duckduckgonewssearch) | **GET** /v1/duckduckgo/news | News search
*DuckDuckGoApi* | [**duckduckgoSearchSuggestions**](docs/Api/DuckDuckGoApi.md#duckduckgosearchsuggestions) | **GET** /v1/duckduckgo/autocomplete | Search suggestions
*DuckDuckGoApi* | [**duckduckgoVideoSearch**](docs/Api/DuckDuckGoApi.md#duckduckgovideosearch) | **GET** /v1/duckduckgo/videos | Video search
*DuckDuckGoApi* | [**duckduckgoWebSearch**](docs/Api/DuckDuckGoApi.md#duckduckgowebsearch) | **GET** /v1/duckduckgo/search | Web search
*EBayApi* | [**ebayBrowseACategory**](docs/Api/EBayApi.md#ebaybrowseacategory) | **GET** /v1/ebay/categories/{category_id}/items | Browse a category
*EBayApi* | [**ebayCompletedSoldListings**](docs/Api/EBayApi.md#ebaycompletedsoldlistings) | **GET** /v1/ebay/completed | Completed / sold listings
*EBayApi* | [**ebayEbayScraperHealthCheck**](docs/Api/EBayApi.md#ebayebayscraperhealthcheck) | **GET** /v1/ebay/health | eBay scraper health check
*EBayApi* | [**ebayEbayScraperHealthCheckHead**](docs/Api/EBayApi.md#ebayebayscraperhealthcheckhead) | **HEAD** /v1/ebay/health | eBay scraper health check
*EBayApi* | [**ebayGetItemDetail**](docs/Api/EBayApi.md#ebaygetitemdetail) | **GET** /v1/ebay/items/{item_id} | Get item detail
*EBayApi* | [**ebayGetItemReviews**](docs/Api/EBayApi.md#ebaygetitemreviews) | **GET** /v1/ebay/items/{item_id}/reviews | Get item reviews
*EBayApi* | [**ebayGetSellerFeedback**](docs/Api/EBayApi.md#ebaygetsellerfeedback) | **GET** /v1/ebay/sellers/{username}/feedback | Get seller feedback
*EBayApi* | [**ebayGetSellerListings**](docs/Api/EBayApi.md#ebaygetsellerlistings) | **GET** /v1/ebay/sellers/{username}/items | Get seller listings
*EBayApi* | [**ebayGetSellerProfile**](docs/Api/EBayApi.md#ebaygetsellerprofile) | **GET** /v1/ebay/sellers/{username} | Get seller profile
*EBayApi* | [**ebayKeywordSuggestions**](docs/Api/EBayApi.md#ebaykeywordsuggestions) | **GET** /v1/ebay/autocomplete | Keyword suggestions
*EBayApi* | [**ebayListCategories**](docs/Api/EBayApi.md#ebaylistcategories) | **GET** /v1/ebay/categories | List categories
*EBayApi* | [**ebayListMarkets**](docs/Api/EBayApi.md#ebaylistmarkets) | **GET** /v1/ebay/markets | List markets
*EBayApi* | [**ebaySearchListings**](docs/Api/EBayApi.md#ebaysearchlistings) | **GET** /v1/ebay/search | Search listings
*FacebookApi* | [**facebookBrowseAMarketplaceCategory**](docs/Api/FacebookApi.md#facebookbrowseamarketplacecategory) | **GET** /v1/facebook/marketplace/category/{category} | Browse a Marketplace category
*FacebookApi* | [**facebookGetAMarketplaceItem**](docs/Api/FacebookApi.md#facebookgetamarketplaceitem) | **GET** /v1/facebook/marketplace/item/{item_id} | Get a Marketplace item
*FacebookApi* | [**facebookGetAdvertiserPageInfo**](docs/Api/FacebookApi.md#facebookgetadvertiserpageinfo) | **GET** /v1/facebook/ads/pages/{page_id} | Get advertiser page info
*FacebookApi* | [**facebookGetAnAd**](docs/Api/FacebookApi.md#facebookgetanad) | **GET** /v1/facebook/ads/{ad_archive_id} | Get an ad
*FacebookApi* | [**facebookGetGroupDetail**](docs/Api/FacebookApi.md#facebookgetgroupdetail) | **GET** /v1/facebook/groups/{group_id} | Get group detail
*FacebookApi* | [**facebookGetGroupPosts**](docs/Api/FacebookApi.md#facebookgetgroupposts) | **GET** /v1/facebook/groups/{group_id}/posts | Get group posts
*FacebookApi* | [**facebookGetPageDetail**](docs/Api/FacebookApi.md#facebookgetpagedetail) | **GET** /v1/facebook/pages/{identifier} | Get page detail
*FacebookApi* | [**facebookGetPagePosts**](docs/Api/FacebookApi.md#facebookgetpageposts) | **GET** /v1/facebook/pages/{identifier}/posts | Get page posts
*FacebookApi* | [**facebookGetPostComments**](docs/Api/FacebookApi.md#facebookgetpostcomments) | **GET** /v1/facebook/posts/{post_id}/comments | Get post comments
*FacebookApi* | [**facebookGetPostDetail**](docs/Api/FacebookApi.md#facebookgetpostdetail) | **GET** /v1/facebook/posts/{post_id} | Get post detail
*FacebookApi* | [**facebookGetProfileDetail**](docs/Api/FacebookApi.md#facebookgetprofiledetail) | **GET** /v1/facebook/profiles/{identifier} | Get profile detail
*FacebookApi* | [**facebookGetProfilePosts**](docs/Api/FacebookApi.md#facebookgetprofileposts) | **GET** /v1/facebook/profiles/{identifier}/posts | Get profile posts
*FacebookApi* | [**facebookListCategories**](docs/Api/FacebookApi.md#facebooklistcategories) | **GET** /v1/facebook/marketplace/categories | List categories
*FacebookApi* | [**facebookListLocations**](docs/Api/FacebookApi.md#facebooklistlocations) | **GET** /v1/facebook/marketplace/locations | List locations
*FacebookApi* | [**facebookSearchAdvertiserPages**](docs/Api/FacebookApi.md#facebooksearchadvertiserpages) | **GET** /v1/facebook/ads/pages/search | Search advertiser pages
*FacebookApi* | [**facebookSearchEvents**](docs/Api/FacebookApi.md#facebooksearchevents) | **GET** /v1/facebook/search/events | Search events
*FacebookApi* | [**facebookSearchEverything**](docs/Api/FacebookApi.md#facebooksearcheverything) | **GET** /v1/facebook/search | Search everything
*FacebookApi* | [**facebookSearchGroups**](docs/Api/FacebookApi.md#facebooksearchgroups) | **GET** /v1/facebook/search/groups | Search groups
*FacebookApi* | [**facebookSearchMarketplace**](docs/Api/FacebookApi.md#facebooksearchmarketplace) | **GET** /v1/facebook/marketplace/search | Search Marketplace
*FacebookApi* | [**facebookSearchPages**](docs/Api/FacebookApi.md#facebooksearchpages) | **GET** /v1/facebook/search/pages | Search Pages
*FacebookApi* | [**facebookSearchPeople**](docs/Api/FacebookApi.md#facebooksearchpeople) | **GET** /v1/facebook/search/people | Search people
*FacebookApi* | [**facebookSearchPlaces**](docs/Api/FacebookApi.md#facebooksearchplaces) | **GET** /v1/facebook/search/places | Search places
*FacebookApi* | [**facebookSearchPosts**](docs/Api/FacebookApi.md#facebooksearchposts) | **GET** /v1/facebook/search/posts | Search posts
*FacebookApi* | [**facebookSearchTheAdLibrary**](docs/Api/FacebookApi.md#facebooksearchtheadlibrary) | **GET** /v1/facebook/ads/search | Search the Ad Library
*GeminiApi* | [**geminiAskGeminiAQuestion**](docs/Api/GeminiApi.md#geminiaskgeminiaquestion) | **GET** /v1/gemini/ask | Ask Gemini a question
*GeminiApi* | [**geminiAskGeminiAQuestionPost**](docs/Api/GeminiApi.md#geminiaskgeminiaquestionpost) | **POST** /v1/gemini/ask | Ask Gemini a question (POST)
*GeminiApi* | [**geminiGeminiScraperHealthCheck**](docs/Api/GeminiApi.md#geminigeminiscraperhealthcheck) | **GET** /v1/gemini/health | Gemini scraper health check
*GeminiApi* | [**geminiGeminiScraperHealthCheckHead**](docs/Api/GeminiApi.md#geminigeminiscraperhealthcheckhead) | **HEAD** /v1/gemini/health | Gemini scraper health check
*GeminiApi* | [**geminiMeasureABrandSVisibilityInAGeminiAnswer**](docs/Api/GeminiApi.md#geminimeasureabrandsvisibilityinageminianswer) | **GET** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer
*GeminiApi* | [**geminiMeasureABrandSVisibilityInAGeminiAnswerPost**](docs/Api/GeminiApi.md#geminimeasureabrandsvisibilityinageminianswerpost) | **POST** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer (POST)
*GoogleApi* | [**googleGetAuthorCitationsPerYearChart**](docs/Api/GoogleApi.md#googlegetauthorcitationsperyearchart) | **GET** /v1/google/scholar/author/citation | Get author citations-per-year chart
*GoogleApi* | [**googleGetBusinessPosts**](docs/Api/GoogleApi.md#googlegetbusinessposts) | **GET** /v1/google/maps/posts | Get business posts
*GoogleApi* | [**googleGetCitationFormatsForAScholarPaper**](docs/Api/GoogleApi.md#googlegetcitationformatsforascholarpaper) | **GET** /v1/google/scholar/cite | Get citation formats for a Scholar paper
*GoogleApi* | [**googleGetPlaceDetails**](docs/Api/GoogleApi.md#googlegetplacedetails) | **GET** /v1/google/maps/place | Get place details
*GoogleApi* | [**googleGetPlacePhotos**](docs/Api/GoogleApi.md#googlegetplacephotos) | **GET** /v1/google/maps/photos | Get place photos
*GoogleApi* | [**googleGetPlaceReviews**](docs/Api/GoogleApi.md#googlegetplacereviews) | **GET** /v1/google/maps/reviews | Get place reviews
*GoogleApi* | [**googleGetScholarAuthorProfile**](docs/Api/GoogleApi.md#googlegetscholarauthorprofile) | **GET** /v1/google/scholar/author | Get Scholar author profile
*GoogleApi* | [**googleGetStockIndexQuote**](docs/Api/GoogleApi.md#googlegetstockindexquote) | **GET** /v1/google/finance/quote | Get stock/index quote
*GoogleApi* | [**googleGoogleAiModeSearch**](docs/Api/GoogleApi.md#googlegoogleaimodesearch) | **GET** /v1/google/ai-mode/search | Google AI Mode search
*GoogleApi* | [**googleGoogleAiOverviewInlineSerpBlock**](docs/Api/GoogleApi.md#googlegoogleaioverviewinlineserpblock) | **GET** /v1/google/ai-overview | Google AI Overview (inline SERP block)
*GoogleApi* | [**googleGoogleFlightsCalendarCheapestFarePerDate**](docs/Api/GoogleApi.md#googlegoogleflightscalendarcheapestfareperdate) | **GET** /v1/google/flights/calendar | Google Flights calendar — cheapest fare per date
*GoogleApi* | [**googleGoogleFlightsSearch**](docs/Api/GoogleApi.md#googlegoogleflightssearch) | **GET** /v1/google/flights/search | Google Flights search
*GoogleApi* | [**googleGoogleLensVisualSearch**](docs/Api/GoogleApi.md#googlegooglelensvisualsearch) | **GET** /v1/google/lens/search | Google Lens visual search
*GoogleApi* | [**googleGoogleScraperHealthCheck**](docs/Api/GoogleApi.md#googlegooglescraperhealthcheck) | **GET** /v1/google/health | Google scraper health check
*GoogleApi* | [**googleGoogleScraperHealthCheckHead**](docs/Api/GoogleApi.md#googlegooglescraperhealthcheckhead) | **HEAD** /v1/google/health | Google scraper health check
*GoogleApi* | [**googleGoogleSearchSuggestions**](docs/Api/GoogleApi.md#googlegooglesearchsuggestions) | **GET** /v1/google/autocomplete | Google search suggestions
*GoogleApi* | [**googleGoogleShortsSearch**](docs/Api/GoogleApi.md#googlegoogleshortssearch) | **GET** /v1/google/shorts/search | Google Shorts search
*GoogleApi* | [**googleGoogleWebSearch**](docs/Api/GoogleApi.md#googlegooglewebsearch) | **GET** /v1/google/search | Google web search
*GoogleApi* | [**googleHotelDetails**](docs/Api/GoogleApi.md#googlehoteldetails) | **GET** /v1/google/hotels/details | Hotel details
*GoogleApi* | [**googleImmersiveProductDetail**](docs/Api/GoogleApi.md#googleimmersiveproductdetail) | **GET** /v1/google/products/detail | Immersive product detail
*GoogleApi* | [**googleInterestByRegion**](docs/Api/GoogleApi.md#googleinterestbyregion) | **GET** /v1/google/trends/regions | Interest by region
*GoogleApi* | [**googleInterestOverTime**](docs/Api/GoogleApi.md#googleinterestovertime) | **GET** /v1/google/trends/interest | Interest over time
*GoogleApi* | [**googleMultiSellerOffersByBarcode**](docs/Api/GoogleApi.md#googlemultiselleroffersbybarcode) | **GET** /v1/google/shopping/offers | Multi-seller offers by barcode
*GoogleApi* | [**googleNewsByTopic**](docs/Api/GoogleApi.md#googlenewsbytopic) | **GET** /v1/google/news/topics | News by topic
*GoogleApi* | [**googlePatentDetails**](docs/Api/GoogleApi.md#googlepatentdetails) | **GET** /v1/google/patents/detail | Patent details
*GoogleApi* | [**googleRelatedTopicsQueries**](docs/Api/GoogleApi.md#googlerelatedtopicsqueries) | **GET** /v1/google/trends/related | Related topics &amp; queries
*GoogleApi* | [**googleSearchGoogleImages**](docs/Api/GoogleApi.md#googlesearchgoogleimages) | **GET** /v1/google/images/search | Search Google Images
*GoogleApi* | [**googleSearchGoogleJobs**](docs/Api/GoogleApi.md#googlesearchgooglejobs) | **GET** /v1/google/jobs/search | Search Google Jobs
*GoogleApi* | [**googleSearchGoogleMapsPlaces**](docs/Api/GoogleApi.md#googlesearchgooglemapsplaces) | **GET** /v1/google/maps/search | Search Google Maps places
*GoogleApi* | [**googleSearchGoogleNews**](docs/Api/GoogleApi.md#googlesearchgooglenews) | **GET** /v1/google/news/search | Search Google News
*GoogleApi* | [**googleSearchGoogleScholar**](docs/Api/GoogleApi.md#googlesearchgooglescholar) | **GET** /v1/google/scholar/search | Search Google Scholar
*GoogleApi* | [**googleSearchGoogleVideos**](docs/Api/GoogleApi.md#googlesearchgooglevideos) | **GET** /v1/google/videos/search | Search Google Videos
*GoogleApi* | [**googleSearchHotels**](docs/Api/GoogleApi.md#googlesearchhotels) | **GET** /v1/google/hotels/search | Search hotels
*GoogleApi* | [**googleSearchPatents**](docs/Api/GoogleApi.md#googlesearchpatents) | **GET** /v1/google/patents/search | Search patents
*GoogleApi* | [**googleSearchProducts**](docs/Api/GoogleApi.md#googlesearchproducts) | **GET** /v1/google/shopping/search | Search products
*GoogleApi* | [**googleSearchScholarAuthorProfiles**](docs/Api/GoogleApi.md#googlesearchscholarauthorprofiles) | **GET** /v1/google/scholar/profiles | Search Scholar author profiles
*GoogleApi* | [**googleTrendingNews**](docs/Api/GoogleApi.md#googletrendingnews) | **GET** /v1/google/news/trending | Trending news
*GoogleApi* | [**googleTrendingSearches**](docs/Api/GoogleApi.md#googletrendingsearches) | **GET** /v1/google/trends/trending | Trending searches
*GoogleApi* | [**googleTrendsTopicAutocomplete**](docs/Api/GoogleApi.md#googletrendstopicautocomplete) | **GET** /v1/google/trends/autocomplete | Trends topic autocomplete
*GooglePlayApi* | [**googlePlayBrowseACategory**](docs/Api/GooglePlayApi.md#googleplaybrowseacategory) | **GET** /v1/google-play/categories/{category_id} | Browse a category
*GooglePlayApi* | [**googlePlayGetAppDetail**](docs/Api/GooglePlayApi.md#googleplaygetappdetail) | **GET** /v1/google-play/apps/{app_id} | Get app detail
*GooglePlayApi* | [**googlePlayGetAppPermissions**](docs/Api/GooglePlayApi.md#googleplaygetapppermissions) | **GET** /v1/google-play/apps/{app_id}/permissions | Get app permissions
*GooglePlayApi* | [**googlePlayGetAppReviews**](docs/Api/GooglePlayApi.md#googleplaygetappreviews) | **GET** /v1/google-play/apps/{app_id}/reviews | Get app reviews
*GooglePlayApi* | [**googlePlayGetDeveloperApps**](docs/Api/GooglePlayApi.md#googleplaygetdeveloperapps) | **GET** /v1/google-play/developers/{developer} | Get developer apps
*GooglePlayApi* | [**googlePlayGetSimilarApps**](docs/Api/GooglePlayApi.md#googleplaygetsimilarapps) | **GET** /v1/google-play/apps/{app_id}/similar | Get similar apps
*GooglePlayApi* | [**googlePlayListCategories**](docs/Api/GooglePlayApi.md#googleplaylistcategories) | **GET** /v1/google-play/categories | List categories
*GooglePlayApi* | [**googlePlayListMarkets**](docs/Api/GooglePlayApi.md#googleplaylistmarkets) | **GET** /v1/google-play/markets | List markets
*GooglePlayApi* | [**googlePlaySearchApps**](docs/Api/GooglePlayApi.md#googleplaysearchapps) | **GET** /v1/google-play/search | Search apps
*GooglePlayApi* | [**googlePlayTopCharts**](docs/Api/GooglePlayApi.md#googleplaytopcharts) | **GET** /v1/google-play/collections/{collection} | Top charts
*IdealistaApi* | [**idealistaAgencyByPhone**](docs/Api/IdealistaApi.md#idealistaagencybyphone) | **GET** /v1/idealista/agency/by-phone/{phone} | Agency by phone
*IdealistaApi* | [**idealistaAgencyProfileListings**](docs/Api/IdealistaApi.md#idealistaagencyprofilelistings) | **GET** /v1/idealista/agency/{short_name} | Agency profile + listings
*IdealistaApi* | [**idealistaGetListingEngagementStats**](docs/Api/IdealistaApi.md#idealistagetlistingengagementstats) | **GET** /v1/idealista/properties/{property_code}/stats | Get listing engagement stats
*IdealistaApi* | [**idealistaGetPropertyDetail**](docs/Api/IdealistaApi.md#idealistagetpropertydetail) | **GET** /v1/idealista/properties/{property_code} | Get property detail
*IdealistaApi* | [**idealistaIdealistaScraperHealthCheck**](docs/Api/IdealistaApi.md#idealistaidealistascraperhealthcheck) | **GET** /v1/idealista/health | Idealista scraper health check
*IdealistaApi* | [**idealistaIdealistaScraperHealthCheckHead**](docs/Api/IdealistaApi.md#idealistaidealistascraperhealthcheckhead) | **HEAD** /v1/idealista/health | Idealista scraper health check
*IdealistaApi* | [**idealistaListMarkets**](docs/Api/IdealistaApi.md#idealistalistmarkets) | **GET** /v1/idealista/markets | List markets
*IdealistaApi* | [**idealistaResolveLocations**](docs/Api/IdealistaApi.md#idealistaresolvelocations) | **GET** /v1/idealista/suggest | Resolve locations
*IdealistaApi* | [**idealistaSearchAllBeatsResultCap**](docs/Api/IdealistaApi.md#idealistasearchallbeatsresultcap) | **GET** /v1/idealista/search/all | Search all (beats result cap)
*IdealistaApi* | [**idealistaSearchListings**](docs/Api/IdealistaApi.md#idealistasearchlistings) | **GET** /v1/idealista/search | Search listings
*ImmobiliareApi* | [**immobiliareGetAgencyProfile**](docs/Api/ImmobiliareApi.md#immobiliaregetagencyprofile) | **GET** /v1/immobiliare/agencies/{agency_id} | Get agency profile
*ImmobiliareApi* | [**immobiliareGetAnAgencySListings**](docs/Api/ImmobiliareApi.md#immobiliaregetanagencyslistings) | **GET** /v1/immobiliare/agencies/{agency_id}/listings | Get an agency&#39;s listings
*ImmobiliareApi* | [**immobiliareGetListingDetail**](docs/Api/ImmobiliareApi.md#immobiliaregetlistingdetail) | **GET** /v1/immobiliare/listings/{listing_id} | Get listing detail
*ImmobiliareApi* | [**immobiliareImmobiliareScraperHealthCheck**](docs/Api/ImmobiliareApi.md#immobiliareimmobiliarescraperhealthcheck) | **GET** /v1/immobiliare/health | Immobiliare scraper health check
*ImmobiliareApi* | [**immobiliareImmobiliareScraperHealthCheckHead**](docs/Api/ImmobiliareApi.md#immobiliareimmobiliarescraperhealthcheckhead) | **HEAD** /v1/immobiliare/health | Immobiliare scraper health check
*ImmobiliareApi* | [**immobiliareListFilterEnums**](docs/Api/ImmobiliareApi.md#immobiliarelistfilterenums) | **GET** /v1/immobiliare/reference | List filter enums
*ImmobiliareApi* | [**immobiliareListMarkets**](docs/Api/ImmobiliareApi.md#immobiliarelistmarkets) | **GET** /v1/immobiliare/markets | List markets
*ImmobiliareApi* | [**immobiliareLocationAutocomplete**](docs/Api/ImmobiliareApi.md#immobiliarelocationautocomplete) | **GET** /v1/immobiliare/autocomplete | Location autocomplete
*ImmobiliareApi* | [**immobiliarePriceMTimeSeries**](docs/Api/ImmobiliareApi.md#immobiliarepricemtimeseries) | **GET** /v1/immobiliare/market-insights/prices | Price €/m² time series
*ImmobiliareApi* | [**immobiliareSearchListings**](docs/Api/ImmobiliareApi.md#immobiliaresearchlistings) | **GET** /v1/immobiliare/search | Search listings
*InstagramApi* | [**instagramAboutThisAccount**](docs/Api/InstagramApi.md#instagramaboutthisaccount) | **GET** /v1/instagram/users/{username}/about | About this account
*InstagramApi* | [**instagramBlendedTopSearch**](docs/Api/InstagramApi.md#instagramblendedtopsearch) | **GET** /v1/instagram/search/top | Blended top search
*InstagramApi* | [**instagramGetActiveStories**](docs/Api/InstagramApi.md#instagramgetactivestories) | **GET** /v1/instagram/users/{username}/stories | Get active stories
*InstagramApi* | [**instagramGetAudioTrack**](docs/Api/InstagramApi.md#instagramgetaudiotrack) | **GET** /v1/instagram/audio/{audio_id} | Get audio track
*InstagramApi* | [**instagramGetComments**](docs/Api/InstagramApi.md#instagramgetcomments) | **GET** /v1/instagram/media/{code}/comments | Get comments
*InstagramApi* | [**instagramGetFollowers**](docs/Api/InstagramApi.md#instagramgetfollowers) | **GET** /v1/instagram/users/{username}/followers | Get followers
*InstagramApi* | [**instagramGetFollowing**](docs/Api/InstagramApi.md#instagramgetfollowing) | **GET** /v1/instagram/users/{username}/following | Get following
*InstagramApi* | [**instagramGetHashtagInfo**](docs/Api/InstagramApi.md#instagramgethashtaginfo) | **GET** /v1/instagram/hashtags/{tag} | Get hashtag info
*InstagramApi* | [**instagramGetHighlights**](docs/Api/InstagramApi.md#instagramgethighlights) | **GET** /v1/instagram/users/{username}/highlights | Get highlights
*InstagramApi* | [**instagramGetLikers**](docs/Api/InstagramApi.md#instagramgetlikers) | **GET** /v1/instagram/media/{code}/likers | Get likers
*InstagramApi* | [**instagramGetLocation**](docs/Api/InstagramApi.md#instagramgetlocation) | **GET** /v1/instagram/locations/{location_pk} | Get location
*InstagramApi* | [**instagramGetPostReelDetail**](docs/Api/InstagramApi.md#instagramgetpostreeldetail) | **GET** /v1/instagram/media/{code} | Get post/reel detail
*InstagramApi* | [**instagramGetProfile**](docs/Api/InstagramApi.md#instagramgetprofile) | **GET** /v1/instagram/users/{username} | Get profile
*InstagramApi* | [**instagramGetTaggedPosts**](docs/Api/InstagramApi.md#instagramgettaggedposts) | **GET** /v1/instagram/users/{username}/tagged | Get tagged posts
*InstagramApi* | [**instagramGetUserPosts**](docs/Api/InstagramApi.md#instagramgetuserposts) | **GET** /v1/instagram/users/{username}/posts | Get user posts
*InstagramApi* | [**instagramGetUserReels**](docs/Api/InstagramApi.md#instagramgetuserreels) | **GET** /v1/instagram/users/{username}/reels | Get user reels
*InstagramApi* | [**instagramHealth**](docs/Api/InstagramApi.md#instagramhealth) | **GET** /v1/instagram/health | Health
*InstagramApi* | [**instagramHealthHead**](docs/Api/InstagramApi.md#instagramhealthhead) | **HEAD** /v1/instagram/health | Health
*InstagramApi* | [**instagramRecentHashtagPosts**](docs/Api/InstagramApi.md#instagramrecenthashtagposts) | **GET** /v1/instagram/hashtags/{tag}/recent | Recent hashtag posts
*InstagramApi* | [**instagramRelatedProfiles**](docs/Api/InstagramApi.md#instagramrelatedprofiles) | **GET** /v1/instagram/users/{username}/related | Related profiles
*InstagramApi* | [**instagramSearchHashtags**](docs/Api/InstagramApi.md#instagramsearchhashtags) | **GET** /v1/instagram/search/hashtags | Search hashtags
*InstagramApi* | [**instagramSearchUsers**](docs/Api/InstagramApi.md#instagramsearchusers) | **GET** /v1/instagram/search/users | Search users
*InstagramApi* | [**instagramTopHashtagPosts**](docs/Api/InstagramApi.md#instagramtophashtagposts) | **GET** /v1/instagram/hashtags/{tag}/top | Top hashtag posts
*LeboncoinApi* | [**leboncoinGetASellerSAds**](docs/Api/LeboncoinApi.md#leboncoingetasellersads) | **GET** /v1/leboncoin/sellers/{user_id}/listings | Get a seller&#39;s ads
*LeboncoinApi* | [**leboncoinGetAdDetail**](docs/Api/LeboncoinApi.md#leboncoingetaddetail) | **GET** /v1/leboncoin/ads/{list_id} | Get ad detail
*LeboncoinApi* | [**leboncoinGetSellerProfile**](docs/Api/LeboncoinApi.md#leboncoingetsellerprofile) | **GET** /v1/leboncoin/sellers/{user_id} | Get seller profile
*LeboncoinApi* | [**leboncoinGetSimilarAds**](docs/Api/LeboncoinApi.md#leboncoingetsimilarads) | **GET** /v1/leboncoin/ads/{list_id}/similar | Get similar ads
*LeboncoinApi* | [**leboncoinLeboncoinScraperHealthCheck**](docs/Api/LeboncoinApi.md#leboncoinleboncoinscraperhealthcheck) | **GET** /v1/leboncoin/health | Leboncoin scraper health check
*LeboncoinApi* | [**leboncoinLeboncoinScraperHealthCheckHead**](docs/Api/LeboncoinApi.md#leboncoinleboncoinscraperhealthcheckhead) | **HEAD** /v1/leboncoin/health | Leboncoin scraper health check
*LeboncoinApi* | [**leboncoinListCategories**](docs/Api/LeboncoinApi.md#leboncoinlistcategories) | **GET** /v1/leboncoin/categories | List categories
*LeboncoinApi* | [**leboncoinListDepartments**](docs/Api/LeboncoinApi.md#leboncoinlistdepartments) | **GET** /v1/leboncoin/departments | List departments
*LeboncoinApi* | [**leboncoinListMarkets**](docs/Api/LeboncoinApi.md#leboncoinlistmarkets) | **GET** /v1/leboncoin/markets | List markets
*LeboncoinApi* | [**leboncoinListRegions**](docs/Api/LeboncoinApi.md#leboncoinlistregions) | **GET** /v1/leboncoin/regions | List regions
*LeboncoinApi* | [**leboncoinLocationAutocomplete**](docs/Api/LeboncoinApi.md#leboncoinlocationautocomplete) | **GET** /v1/leboncoin/locations/search | Location autocomplete
*LeboncoinApi* | [**leboncoinSearchLeboncoinAds**](docs/Api/LeboncoinApi.md#leboncoinsearchleboncoinads) | **GET** /v1/leboncoin/search | Search Leboncoin ads
*LinkedInApi* | [**linkedinGetACompanySJobPostings**](docs/Api/LinkedInApi.md#linkedingetacompanysjobpostings) | **GET** /v1/linkedin/companies/{company_id}/jobs | Get a company&#39;s job postings
*LinkedInApi* | [**linkedinGetACourse**](docs/Api/LinkedInApi.md#linkedingetacourse) | **GET** /v1/linkedin/learning/{course_slug} | Get a course
*LinkedInApi* | [**linkedinGetAPublicArticle**](docs/Api/LinkedInApi.md#linkedingetapublicarticle) | **GET** /v1/linkedin/articles/{article_slug} | Get a public article
*LinkedInApi* | [**linkedinGetAPublicPost**](docs/Api/LinkedInApi.md#linkedingetapublicpost) | **GET** /v1/linkedin/posts/{post_slug} | Get a public post
*LinkedInApi* | [**linkedinGetCompany**](docs/Api/LinkedInApi.md#linkedingetcompany) | **GET** /v1/linkedin/companies/{universal_name} | Get company
*LinkedInApi* | [**linkedinGetJobDetail**](docs/Api/LinkedInApi.md#linkedingetjobdetail) | **GET** /v1/linkedin/jobs/{job_id} | Get job detail
*LinkedInApi* | [**linkedinGetPublicProfile**](docs/Api/LinkedInApi.md#linkedingetpublicprofile) | **GET** /v1/linkedin/profiles/{public_id} | Get public profile
*LinkedInApi* | [**linkedinGetSchool**](docs/Api/LinkedInApi.md#linkedingetschool) | **GET** /v1/linkedin/schools/{universal_name} | Get school
*LinkedInApi* | [**linkedinLinkedinScraperHealthCheck**](docs/Api/LinkedInApi.md#linkedinlinkedinscraperhealthcheck) | **GET** /v1/linkedin/health | LinkedIn scraper health check
*LinkedInApi* | [**linkedinLinkedinScraperHealthCheckHead**](docs/Api/LinkedInApi.md#linkedinlinkedinscraperhealthcheckhead) | **HEAD** /v1/linkedin/health | LinkedIn scraper health check
*LinkedInApi* | [**linkedinSearchLinkedinJobs**](docs/Api/LinkedInApi.md#linkedinsearchlinkedinjobs) | **GET** /v1/linkedin/jobs/search | Search LinkedIn jobs
*LinkedInApi* | [**linkedinSuggestLocationGeoIds**](docs/Api/LinkedInApi.md#linkedinsuggestlocationgeoids) | **GET** /v1/linkedin/geo/suggest | Suggest location geo ids
*LoopNetApi* | [**loopnetGetBrokerProfile**](docs/Api/LoopNetApi.md#loopnetgetbrokerprofile) | **GET** /v1/loopnet/brokers/{slug}/{broker_id} | Get broker profile
*LoopNetApi* | [**loopnetGetListingDetail**](docs/Api/LoopNetApi.md#loopnetgetlistingdetail) | **GET** /v1/loopnet/listings/{listing_id} | Get listing detail
*LoopNetApi* | [**loopnetListCoverageMarkets**](docs/Api/LoopNetApi.md#loopnetlistcoveragemarkets) | **GET** /v1/loopnet/markets | List coverage markets
*LoopNetApi* | [**loopnetListPropertyTypes**](docs/Api/LoopNetApi.md#loopnetlistpropertytypes) | **GET** /v1/loopnet/property-types | List property types
*LoopNetApi* | [**loopnetLoopnetScraperHealthCheck**](docs/Api/LoopNetApi.md#loopnetloopnetscraperhealthcheck) | **GET** /v1/loopnet/health | LoopNet scraper health check
*LoopNetApi* | [**loopnetLoopnetScraperHealthCheckHead**](docs/Api/LoopNetApi.md#loopnetloopnetscraperhealthcheckhead) | **HEAD** /v1/loopnet/health | LoopNet scraper health check
*LoopNetApi* | [**loopnetSearchCommercialRealEstate**](docs/Api/LoopNetApi.md#loopnetsearchcommercialrealestate) | **GET** /v1/loopnet/search | Search commercial real estate
*PerplexityApi* | [**perplexityAskPerplexityAQuestion**](docs/Api/PerplexityApi.md#perplexityaskperplexityaquestion) | **GET** /v1/perplexity/ask | Ask Perplexity a question
*PerplexityApi* | [**perplexityAskPerplexityAQuestionPost**](docs/Api/PerplexityApi.md#perplexityaskperplexityaquestionpost) | **POST** /v1/perplexity/ask | Ask Perplexity a question (POST)
*PerplexityApi* | [**perplexityMeasureABrandSVisibilityInAPerplexityAnswer**](docs/Api/PerplexityApi.md#perplexitymeasureabrandsvisibilityinaperplexityanswer) | **GET** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer
*PerplexityApi* | [**perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost**](docs/Api/PerplexityApi.md#perplexitymeasureabrandsvisibilityinaperplexityanswerpost) | **POST** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer (POST)
*PerplexityApi* | [**perplexityPerplexityScraperHealthCheck**](docs/Api/PerplexityApi.md#perplexityperplexityscraperhealthcheck) | **GET** /v1/perplexity/health | Perplexity scraper health check
*PerplexityApi* | [**perplexityPerplexityScraperHealthCheckHead**](docs/Api/PerplexityApi.md#perplexityperplexityscraperhealthcheckhead) | **HEAD** /v1/perplexity/health | Perplexity scraper health check
*RealtorApi* | [**realtorGetFullPropertyDetail**](docs/Api/RealtorApi.md#realtorgetfullpropertydetail) | **GET** /v1/realtor/properties/{property_id} | Get full property detail
*RealtorApi* | [**realtorListMarkets**](docs/Api/RealtorApi.md#realtorlistmarkets) | **GET** /v1/realtor/markets | List markets
*RealtorApi* | [**realtorLocationAutocomplete**](docs/Api/RealtorApi.md#realtorlocationautocomplete) | **GET** /v1/realtor/autocomplete | Location autocomplete
*RealtorApi* | [**realtorRealtorScraperHealthCheck**](docs/Api/RealtorApi.md#realtorrealtorscraperhealthcheck) | **GET** /v1/realtor/health | Realtor scraper health check
*RealtorApi* | [**realtorRealtorScraperHealthCheckHead**](docs/Api/RealtorApi.md#realtorrealtorscraperhealthcheckhead) | **HEAD** /v1/realtor/health | Realtor scraper health check
*RealtorApi* | [**realtorSearchPropertyListings**](docs/Api/RealtorApi.md#realtorsearchpropertylistings) | **GET** /v1/realtor/search | Search property listings
*RedditApi* | [**redditGetCrossPosts**](docs/Api/RedditApi.md#redditgetcrossposts) | **GET** /v1/reddit/posts/{post_id}/duplicates | Get cross-posts
*RedditApi* | [**redditGetPostComments**](docs/Api/RedditApi.md#redditgetpostcomments) | **GET** /v1/reddit/posts/{post_id}/comments | Get post comments
*RedditApi* | [**redditGetPostDetail**](docs/Api/RedditApi.md#redditgetpostdetail) | **GET** /v1/reddit/posts/{post_id} | Get post detail
*RedditApi* | [**redditGetPostsByDomain**](docs/Api/RedditApi.md#redditgetpostsbydomain) | **GET** /v1/reddit/domains/{domain}/posts | Get posts by domain
*RedditApi* | [**redditGetSubredditInfo**](docs/Api/RedditApi.md#redditgetsubredditinfo) | **GET** /v1/reddit/subreddits/{subreddit} | Get subreddit info
*RedditApi* | [**redditGetSubredditPosts**](docs/Api/RedditApi.md#redditgetsubredditposts) | **GET** /v1/reddit/subreddits/{subreddit}/posts | Get subreddit posts
*RedditApi* | [**redditGetSubredditRules**](docs/Api/RedditApi.md#redditgetsubredditrules) | **GET** /v1/reddit/subreddits/{subreddit}/rules | Get subreddit rules
*RedditApi* | [**redditGetTrendingPosts**](docs/Api/RedditApi.md#redditgettrendingposts) | **GET** /v1/reddit/posts/trending | Get trending posts
*RedditApi* | [**redditGetUserProfile**](docs/Api/RedditApi.md#redditgetuserprofile) | **GET** /v1/reddit/users/{username} | Get user profile
*RedditApi* | [**redditGetUserSComments**](docs/Api/RedditApi.md#redditgetuserscomments) | **GET** /v1/reddit/users/{username}/comments | Get user&#39;s comments
*RedditApi* | [**redditGetUserSModeratedSubreddits**](docs/Api/RedditApi.md#redditgetusersmoderatedsubreddits) | **GET** /v1/reddit/users/{username}/moderated | Get user&#39;s moderated subreddits
*RedditApi* | [**redditGetUserSPosts**](docs/Api/RedditApi.md#redditgetusersposts) | **GET** /v1/reddit/users/{username}/posts | Get user&#39;s posts
*RedditApi* | [**redditGetUserSTrophies**](docs/Api/RedditApi.md#redditgetuserstrophies) | **GET** /v1/reddit/users/{username}/trophies | Get user&#39;s trophies
*RedditApi* | [**redditGetWikiPageContent**](docs/Api/RedditApi.md#redditgetwikipagecontent) | **GET** /v1/reddit/subreddits/{subreddit}/wiki/{page} | Get wiki page content
*RedditApi* | [**redditListWikiPages**](docs/Api/RedditApi.md#redditlistwikipages) | **GET** /v1/reddit/subreddits/{subreddit}/wiki | List wiki pages
*RedditApi* | [**redditNewSubreddits**](docs/Api/RedditApi.md#redditnewsubreddits) | **GET** /v1/reddit/subreddits/new | New subreddits
*RedditApi* | [**redditPopularSubreddits**](docs/Api/RedditApi.md#redditpopularsubreddits) | **GET** /v1/reddit/subreddits/popular | Popular subreddits
*RedditApi* | [**redditRedditScraperHealthCheck**](docs/Api/RedditApi.md#redditredditscraperhealthcheck) | **GET** /v1/reddit/health | Reddit scraper health check
*RedditApi* | [**redditRedditScraperHealthCheckHead**](docs/Api/RedditApi.md#redditredditscraperhealthcheckhead) | **HEAD** /v1/reddit/health | Reddit scraper health check
*RedditApi* | [**redditSearchRedditPosts**](docs/Api/RedditApi.md#redditsearchredditposts) | **GET** /v1/reddit/search/posts | Search Reddit posts
*RedditApi* | [**redditSearchSubreddits**](docs/Api/RedditApi.md#redditsearchsubreddits) | **GET** /v1/reddit/search/subreddits | Search subreddits
*RedditApi* | [**redditSearchUsers**](docs/Api/RedditApi.md#redditsearchusers) | **GET** /v1/reddit/search/users | Search users
*RedfinApi* | [**redfinGetAgentProfileListings**](docs/Api/RedfinApi.md#redfingetagentprofilelistings) | **GET** /v1/redfin/agent | Get agent profile + listings
*RedfinApi* | [**redfinGetPropertyDetail**](docs/Api/RedfinApi.md#redfingetpropertydetail) | **GET** /v1/redfin/property/{property_id} | Get property detail
*RedfinApi* | [**redfinGetPropertyDetailByUrl**](docs/Api/RedfinApi.md#redfingetpropertydetailbyurl) | **GET** /v1/redfin/property | Get property detail by URL
*RedfinApi* | [**redfinListCoverageMarkets**](docs/Api/RedfinApi.md#redfinlistcoveragemarkets) | **GET** /v1/redfin/markets | List coverage markets
*RedfinApi* | [**redfinRedfinScraperHealthCheck**](docs/Api/RedfinApi.md#redfinredfinscraperhealthcheck) | **GET** /v1/redfin/health | Redfin scraper health check
*RedfinApi* | [**redfinRedfinScraperHealthCheckHead**](docs/Api/RedfinApi.md#redfinredfinscraperhealthcheckhead) | **HEAD** /v1/redfin/health | Redfin scraper health check
*RedfinApi* | [**redfinRegionAddressSuggestions**](docs/Api/RedfinApi.md#redfinregionaddresssuggestions) | **GET** /v1/redfin/autocomplete | Region/address suggestions
*RedfinApi* | [**redfinSearchProperties**](docs/Api/RedfinApi.md#redfinsearchproperties) | **GET** /v1/redfin/search | Search properties
*TikTokApi* | [**tiktokGeneralSearch**](docs/Api/TikTokApi.md#tiktokgeneralsearch) | **GET** /v1/tiktok/search | General search
*TikTokApi* | [**tiktokGetCommentReplies**](docs/Api/TikTokApi.md#tiktokgetcommentreplies) | **GET** /v1/tiktok/comments/{comment_id}/replies | Get comment replies
*TikTokApi* | [**tiktokGetComments**](docs/Api/TikTokApi.md#tiktokgetcomments) | **GET** /v1/tiktok/videos/{video_id}/comments | Get comments
*TikTokApi* | [**tiktokGetFollowersDeprecated**](docs/Api/TikTokApi.md#tiktokgetfollowersdeprecated) | **GET** /v1/tiktok/users/{username}/followers | Get followers (deprecated)
*TikTokApi* | [**tiktokGetFollowingDeprecated**](docs/Api/TikTokApi.md#tiktokgetfollowingdeprecated) | **GET** /v1/tiktok/users/{username}/following | Get following (deprecated)
*TikTokApi* | [**tiktokGetHashtagDetail**](docs/Api/TikTokApi.md#tiktokgethashtagdetail) | **GET** /v1/tiktok/hashtags/{name} | Get hashtag detail
*TikTokApi* | [**tiktokGetHashtagVideos**](docs/Api/TikTokApi.md#tiktokgethashtagvideos) | **GET** /v1/tiktok/hashtags/{name}/videos | Get hashtag videos
*TikTokApi* | [**tiktokGetLikedVideosDeprecated**](docs/Api/TikTokApi.md#tiktokgetlikedvideosdeprecated) | **GET** /v1/tiktok/users/{username}/liked | Get liked videos (deprecated)
*TikTokApi* | [**tiktokGetMusicSoundDetail**](docs/Api/TikTokApi.md#tiktokgetmusicsounddetail) | **GET** /v1/tiktok/music/{music_id} | Get music/sound detail
*TikTokApi* | [**tiktokGetMusicVideos**](docs/Api/TikTokApi.md#tiktokgetmusicvideos) | **GET** /v1/tiktok/music/{music_id}/videos | Get music videos
*TikTokApi* | [**tiktokGetOembedMetadata**](docs/Api/TikTokApi.md#tiktokgetoembedmetadata) | **GET** /v1/tiktok/oembed | Get oEmbed metadata
*TikTokApi* | [**tiktokGetRelatedVideos**](docs/Api/TikTokApi.md#tiktokgetrelatedvideos) | **GET** /v1/tiktok/videos/{video_id}/related | Get related videos
*TikTokApi* | [**tiktokGetReposts**](docs/Api/TikTokApi.md#tiktokgetreposts) | **GET** /v1/tiktok/users/{username}/reposts | Get reposts
*TikTokApi* | [**tiktokGetTiktokAdDetail**](docs/Api/TikTokApi.md#tiktokgettiktokaddetail) | **GET** /v1/tiktok/ads/{ad_id} | Get TikTok ad detail
*TikTokApi* | [**tiktokGetTranscript**](docs/Api/TikTokApi.md#tiktokgettranscript) | **GET** /v1/tiktok/videos/{video_id}/transcript | Get transcript
*TikTokApi* | [**tiktokGetUserProfile**](docs/Api/TikTokApi.md#tiktokgetuserprofile) | **GET** /v1/tiktok/users/{username} | Get user profile
*TikTokApi* | [**tiktokGetUserVideos**](docs/Api/TikTokApi.md#tiktokgetuservideos) | **GET** /v1/tiktok/users/{username}/videos | Get user videos
*TikTokApi* | [**tiktokGetVideoDetail**](docs/Api/TikTokApi.md#tiktokgetvideodetail) | **GET** /v1/tiktok/videos/{video_id} | Get video detail
*TikTokApi* | [**tiktokHealthCheck**](docs/Api/TikTokApi.md#tiktokhealthcheck) | **GET** /v1/tiktok/health | Health check
*TikTokApi* | [**tiktokHealthCheckHead**](docs/Api/TikTokApi.md#tiktokhealthcheckhead) | **HEAD** /v1/tiktok/health | Health check
*TikTokApi* | [**tiktokListRegions**](docs/Api/TikTokApi.md#tiktoklistregions) | **GET** /v1/tiktok/regions | List regions
*TikTokApi* | [**tiktokSearchHashtags**](docs/Api/TikTokApi.md#tiktoksearchhashtags) | **GET** /v1/tiktok/search/hashtags | Search hashtags
*TikTokApi* | [**tiktokSearchTheTiktokAdLibrary**](docs/Api/TikTokApi.md#tiktoksearchthetiktokadlibrary) | **GET** /v1/tiktok/ads/search | Search the TikTok Ad Library
*TikTokApi* | [**tiktokSearchTiktokAdvertisers**](docs/Api/TikTokApi.md#tiktoksearchtiktokadvertisers) | **GET** /v1/tiktok/ads/advertisers | Search TikTok advertisers
*TikTokApi* | [**tiktokSearchUsers**](docs/Api/TikTokApi.md#tiktoksearchusers) | **GET** /v1/tiktok/search/users | Search users
*TikTokApi* | [**tiktokSearchVideos**](docs/Api/TikTokApi.md#tiktoksearchvideos) | **GET** /v1/tiktok/search/videos | Search videos
*TikTokApi* | [**tiktokTrendingHashtags**](docs/Api/TikTokApi.md#tiktoktrendinghashtags) | **GET** /v1/tiktok/trending/hashtags | Trending hashtags
*TikTokApi* | [**tiktokTrendingSongs**](docs/Api/TikTokApi.md#tiktoktrendingsongs) | **GET** /v1/tiktok/trending/songs | Trending songs
*TikTokApi* | [**tiktokTrendingVideos**](docs/Api/TikTokApi.md#tiktoktrendingvideos) | **GET** /v1/tiktok/trending/videos | Trending videos
*TwitterApi* | [**twitterAdvancedTweetSearch**](docs/Api/TwitterApi.md#twitteradvancedtweetsearch) | **GET** /v1/twitter/tweets/advanced_search | Advanced tweet search
*TwitterApi* | [**twitterBatchGetUsersByIds**](docs/Api/TwitterApi.md#twitterbatchgetusersbyids) | **GET** /v1/twitter/users/batch_by_ids | Batch get users by IDs
*TwitterApi* | [**twitterBatchGetUsersByUsernames**](docs/Api/TwitterApi.md#twitterbatchgetusersbyusernames) | **GET** /v1/twitter/users/batch_by_usernames | Batch get users by usernames
*TwitterApi* | [**twitterConfigureWebhookOnAMonitor**](docs/Api/TwitterApi.md#twitterconfigurewebhookonamonitor) | **POST** /v1/twitter/stream/webhooks | Configure webhook on a monitor
*TwitterApi* | [**twitterCreateFilterRule**](docs/Api/TwitterApi.md#twittercreatefilterrule) | **POST** /v1/twitter/stream/filter-rules | Create filter rule
*TwitterApi* | [**twitterCreateStreamMonitor**](docs/Api/TwitterApi.md#twittercreatestreammonitor) | **POST** /v1/twitter/stream/monitors | Create stream monitor
*TwitterApi* | [**twitterDeleteFilterRule**](docs/Api/TwitterApi.md#twitterdeletefilterrule) | **DELETE** /v1/twitter/stream/filter-rules/{rule_id} | Delete filter rule
*TwitterApi* | [**twitterDeleteStreamMonitor**](docs/Api/TwitterApi.md#twitterdeletestreammonitor) | **DELETE** /v1/twitter/stream/monitors/{monitor_id} | Delete stream monitor
*TwitterApi* | [**twitterGetArticleById**](docs/Api/TwitterApi.md#twittergetarticlebyid) | **GET** /v1/twitter/tweets/article/{article_id} | Get article by ID
*TwitterApi* | [**twitterGetBroadcastDetails**](docs/Api/TwitterApi.md#twittergetbroadcastdetails) | **GET** /v1/twitter/spaces/broadcast/{broadcast_id} | Get broadcast details
*TwitterApi* | [**twitterGetCommunityDetails**](docs/Api/TwitterApi.md#twittergetcommunitydetails) | **GET** /v1/twitter/communities/{community_id} | Get community details
*TwitterApi* | [**twitterGetCommunityNotes**](docs/Api/TwitterApi.md#twittergetcommunitynotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/community_notes | Get community notes
*TwitterApi* | [**twitterGetCommunityTweets**](docs/Api/TwitterApi.md#twittergetcommunitytweets) | **GET** /v1/twitter/communities/{community_id}/tweets | Get community tweets
*TwitterApi* | [**twitterGetFilterRule**](docs/Api/TwitterApi.md#twittergetfilterrule) | **GET** /v1/twitter/stream/filter-rules/{rule_id} | Get filter rule
*TwitterApi* | [**twitterGetFilterRulePerPollRates**](docs/Api/TwitterApi.md#twittergetfilterruleperpollrates) | **GET** /v1/twitter/stream/filter-rules-pricing | Get filter rule per-poll rates
*TwitterApi* | [**twitterGetListDetails**](docs/Api/TwitterApi.md#twittergetlistdetails) | **GET** /v1/twitter/lists/{list_id}/detail | Get list details
*TwitterApi* | [**twitterGetListTweets**](docs/Api/TwitterApi.md#twittergetlisttweets) | **GET** /v1/twitter/lists/{list_id}/tweets | Get list tweets
*TwitterApi* | [**twitterGetPlaceDetails**](docs/Api/TwitterApi.md#twittergetplacedetails) | **GET** /v1/twitter/geo/places/{place_id} | Get place details
*TwitterApi* | [**twitterGetSimilarTweets**](docs/Api/TwitterApi.md#twittergetsimilartweets) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/similar | Get similar tweets
*TwitterApi* | [**twitterGetSpaceDetails**](docs/Api/TwitterApi.md#twittergetspacedetails) | **GET** /v1/twitter/spaces/{space_id} | Get Space details
*TwitterApi* | [**twitterGetStreamMonitor**](docs/Api/TwitterApi.md#twittergetstreammonitor) | **GET** /v1/twitter/stream/monitors/{monitor_id} | Get stream monitor
*TwitterApi* | [**twitterGetTrendingTopics**](docs/Api/TwitterApi.md#twittergettrendingtopics) | **GET** /v1/twitter/trends/ | Get trending topics
*TwitterApi* | [**twitterGetTrendsByLocation**](docs/Api/TwitterApi.md#twittergettrendsbylocation) | **GET** /v1/twitter/trends/place/{woeid} | Get trends by location
*TwitterApi* | [**twitterGetTweetDetails**](docs/Api/TwitterApi.md#twittergettweetdetails) | **GET** /v1/twitter/tweets/tweet/{tweet_id} | Get tweet details
*TwitterApi* | [**twitterGetTweetEditHistory**](docs/Api/TwitterApi.md#twittergettweetedithistory) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/edit_history | Get tweet edit history
*TwitterApi* | [**twitterGetTweetFavoriters**](docs/Api/TwitterApi.md#twittergettweetfavoriters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/favoriters | Get tweet favoriters
*TwitterApi* | [**twitterGetTweetQuotes**](docs/Api/TwitterApi.md#twittergettweetquotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/quotes | Get tweet quotes
*TwitterApi* | [**twitterGetTweetReplies**](docs/Api/TwitterApi.md#twittergettweetreplies) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/replies | Get tweet replies
*TwitterApi* | [**twitterGetTweetRetweeters**](docs/Api/TwitterApi.md#twittergettweetretweeters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/retweeters | Get tweet retweeters
*TwitterApi* | [**twitterGetTweetsByIds**](docs/Api/TwitterApi.md#twittergettweetsbyids) | **GET** /v1/twitter/tweets/ | Get tweets by IDs
*TwitterApi* | [**twitterGetUserArticles**](docs/Api/TwitterApi.md#twittergetuserarticles) | **GET** /v1/twitter/users/{user_id}/articles | Get user articles
*TwitterApi* | [**twitterGetUserById**](docs/Api/TwitterApi.md#twittergetuserbyid) | **GET** /v1/twitter/users/{user_id}/by_id | Get user by ID
*TwitterApi* | [**twitterGetUserByUsername**](docs/Api/TwitterApi.md#twittergetuserbyusername) | **GET** /v1/twitter/users/{username}/by_username | Get user by username
*TwitterApi* | [**twitterGetUserFollowers**](docs/Api/TwitterApi.md#twittergetuserfollowers) | **GET** /v1/twitter/users/{username}/followers | Get user followers
*TwitterApi* | [**twitterGetUserFollowing**](docs/Api/TwitterApi.md#twittergetuserfollowing) | **GET** /v1/twitter/users/{username}/followings | Get user following
*TwitterApi* | [**twitterGetUserMentions**](docs/Api/TwitterApi.md#twittergetusermentions) | **GET** /v1/twitter/users/{username}/mentions | Get user mentions
*TwitterApi* | [**twitterGetUserSubscriptions**](docs/Api/TwitterApi.md#twittergetusersubscriptions) | **GET** /v1/twitter/users/{user_id}/subscriptions | Get user subscriptions
*TwitterApi* | [**twitterGetUserTweets**](docs/Api/TwitterApi.md#twittergetusertweets) | **GET** /v1/twitter/users/{username}/latest_tweets | Get user tweets
*TwitterApi* | [**twitterListBillingLogs**](docs/Api/TwitterApi.md#twitterlistbillinglogs) | **GET** /v1/twitter/stream/billing-logs | List billing logs
*TwitterApi* | [**twitterListDeliveryLogsForAFilterRule**](docs/Api/TwitterApi.md#twitterlistdeliverylogsforafilterrule) | **GET** /v1/twitter/stream/filter-rules/{rule_id}/logs | List delivery logs for a filter rule
*TwitterApi* | [**twitterListFilterRules**](docs/Api/TwitterApi.md#twitterlistfilterrules) | **GET** /v1/twitter/stream/filter-rules | List filter rules
*TwitterApi* | [**twitterListStreamMonitors**](docs/Api/TwitterApi.md#twitterliststreammonitors) | **GET** /v1/twitter/stream/monitors | List stream monitors
*TwitterApi* | [**twitterListTweetDeliveryLogs**](docs/Api/TwitterApi.md#twitterlisttweetdeliverylogs) | **GET** /v1/twitter/stream/logs | List tweet delivery logs
*TwitterApi* | [**twitterListWebhooks**](docs/Api/TwitterApi.md#twitterlistwebhooks) | **GET** /v1/twitter/stream/webhooks | List webhooks
*TwitterApi* | [**twitterRemoveWebhookFromMonitor**](docs/Api/TwitterApi.md#twitterremovewebhookfrommonitor) | **DELETE** /v1/twitter/stream/webhooks/{webhook_id} | Remove webhook from monitor
*TwitterApi* | [**twitterSearchCommunities**](docs/Api/TwitterApi.md#twittersearchcommunities) | **GET** /v1/twitter/communities/search | Search communities
*TwitterApi* | [**twitterSearchListTweets**](docs/Api/TwitterApi.md#twittersearchlisttweets) | **GET** /v1/twitter/lists/{list_id}/search_tweets | Search list tweets
*TwitterApi* | [**twitterSearchPlaces**](docs/Api/TwitterApi.md#twittersearchplaces) | **GET** /v1/twitter/geo/search | Search places
*TwitterApi* | [**twitterSearchUsers**](docs/Api/TwitterApi.md#twittersearchusers) | **GET** /v1/twitter/users/search_users | Search users
*TwitterApi* | [**twitterTestWebhookDelivery**](docs/Api/TwitterApi.md#twittertestwebhookdelivery) | **POST** /v1/twitter/stream/webhooks/test | Test webhook delivery
*TwitterApi* | [**twitterTwitterScraperHealthCheck**](docs/Api/TwitterApi.md#twittertwitterscraperhealthcheck) | **GET** /v1/twitter/health | Twitter scraper health check
*TwitterApi* | [**twitterTwitterScraperHealthCheckHead**](docs/Api/TwitterApi.md#twittertwitterscraperhealthcheckhead) | **HEAD** /v1/twitter/health | Twitter scraper health check
*TwitterApi* | [**twitterUpdateFilterRule**](docs/Api/TwitterApi.md#twitterupdatefilterrule) | **PATCH** /v1/twitter/stream/filter-rules/{rule_id} | Update filter rule
*TwitterApi* | [**twitterUpdateStreamMonitor**](docs/Api/TwitterApi.md#twitterupdatestreammonitor) | **PATCH** /v1/twitter/stream/monitors/{monitor_id} | Update stream monitor
*TwitterApi* | [**twitterValidateSearchQuery**](docs/Api/TwitterApi.md#twittervalidatesearchquery) | **POST** /v1/twitter/stream/filter-rules/validate | Validate search query
*VintedApi* | [**vintedGetItemDetails**](docs/Api/VintedApi.md#vintedgetitemdetails) | **GET** /v1/vinted/items/{item_id} | Get item details
*VintedApi* | [**vintedGetUserProfile**](docs/Api/VintedApi.md#vintedgetuserprofile) | **GET** /v1/vinted/users/{user_id} | Get user profile
*VintedApi* | [**vintedGetUserSListedItems**](docs/Api/VintedApi.md#vintedgetuserslisteditems) | **GET** /v1/vinted/users/{user_id}/items | Get user&#39;s listed items
*VintedApi* | [**vintedListColors**](docs/Api/VintedApi.md#vintedlistcolors) | **GET** /v1/vinted/colors | List colors
*VintedApi* | [**vintedListItemConditions**](docs/Api/VintedApi.md#vintedlistitemconditions) | **GET** /v1/vinted/statuses | List item conditions
*VintedApi* | [**vintedListMarkets**](docs/Api/VintedApi.md#vintedlistmarkets) | **GET** /v1/vinted/markets | List markets
*VintedApi* | [**vintedSearchBrands**](docs/Api/VintedApi.md#vintedsearchbrands) | **GET** /v1/vinted/brands | Search brands
*VintedApi* | [**vintedSearchVintedItems**](docs/Api/VintedApi.md#vintedsearchvinteditems) | **GET** /v1/vinted/search | Search Vinted items
*VintedApi* | [**vintedVintedScraperHealthCheck**](docs/Api/VintedApi.md#vintedvintedscraperhealthcheck) | **GET** /v1/vinted/health | Vinted scraper health check
*VintedApi* | [**vintedVintedScraperHealthCheckHead**](docs/Api/VintedApi.md#vintedvintedscraperhealthcheckhead) | **HEAD** /v1/vinted/health | Vinted scraper health check
*WalmartApi* | [**walmartBrowseACategory**](docs/Api/WalmartApi.md#walmartbrowseacategory) | **GET** /v1/walmart/category | Browse a category
*WalmartApi* | [**walmartDealsRollbacksAndClearance**](docs/Api/WalmartApi.md#walmartdealsrollbacksandclearance) | **GET** /v1/walmart/deals | Deals, rollbacks and clearance
*WalmartApi* | [**walmartGetASellerSCatalogue**](docs/Api/WalmartApi.md#walmartgetasellerscatalogue) | **GET** /v1/walmart/sellers/{seller_id}/products | Get a seller&#39;s catalogue
*WalmartApi* | [**walmartGetProductDetail**](docs/Api/WalmartApi.md#walmartgetproductdetail) | **GET** /v1/walmart/products/{item_id} | Get product detail
*WalmartApi* | [**walmartGetProductReviews**](docs/Api/WalmartApi.md#walmartgetproductreviews) | **GET** /v1/walmart/products/{item_id}/reviews | Get product reviews
*WalmartApi* | [**walmartGetSellerProfile**](docs/Api/WalmartApi.md#walmartgetsellerprofile) | **GET** /v1/walmart/sellers/{seller_id} | Get seller profile
*WalmartApi* | [**walmartGetStoreNearbyStores**](docs/Api/WalmartApi.md#walmartgetstorenearbystores) | **GET** /v1/walmart/stores/{store_id} | Get store + nearby stores
*WalmartApi* | [**walmartListSupportedMarkets**](docs/Api/WalmartApi.md#walmartlistsupportedmarkets) | **GET** /v1/walmart/markets | List supported markets
*WalmartApi* | [**walmartSearchProducts**](docs/Api/WalmartApi.md#walmartsearchproducts) | **GET** /v1/walmart/search | Search products
*WalmartApi* | [**walmartSearchSuggestions**](docs/Api/WalmartApi.md#walmartsearchsuggestions) | **GET** /v1/walmart/autocomplete | Search suggestions
*WalmartApi* | [**walmartWalmartScraperHealthCheck**](docs/Api/WalmartApi.md#walmartwalmartscraperhealthcheck) | **GET** /v1/walmart/health | Walmart scraper health check
*WalmartApi* | [**walmartWalmartScraperHealthCheckHead**](docs/Api/WalmartApi.md#walmartwalmartscraperhealthcheckhead) | **HEAD** /v1/walmart/health | Walmart scraper health check
*WebApi* | [**webDetectAntiBotAndCaptchaSystems**](docs/Api/WebApi.md#webdetectantibotandcaptchasystems) | **POST** /v1/web/detect | Detect anti-bot and CAPTCHA systems
*WebApi* | [**webExtractStructuredData**](docs/Api/WebApi.md#webextractstructureddata) | **POST** /v1/web/extract | Extract structured data
*WebApi* | [**webGetBatchJobStatus**](docs/Api/WebApi.md#webgetbatchjobstatus) | **GET** /v1/web/batch/{job_id} | Get batch job status
*WebApi* | [**webPollAnAutoUnblockDiscoveryJob**](docs/Api/WebApi.md#webpollanautounblockdiscoveryjob) | **GET** /v1/web/unblock/{job_id} | Poll an auto-unblock discovery job
*WebApi* | [**webScrapeAUrl**](docs/Api/WebApi.md#webscrapeaurl) | **POST** /v1/web/scrape | Scrape a URL
*WebApi* | [**webSubmitBatchScrapingJob**](docs/Api/WebApi.md#websubmitbatchscrapingjob) | **POST** /v1/web/batch | Submit batch scraping job
*WebApi* | [**webTakeAScreenshot**](docs/Api/WebApi.md#webtakeascreenshot) | **POST** /v1/web/screenshot | Take a screenshot
*WebApi* | [**webWebScraperHealthCheck**](docs/Api/WebApi.md#webwebscraperhealthcheck) | **GET** /v1/web/health | Web scraper health check
*WebApi* | [**webWebScraperHealthCheckHead**](docs/Api/WebApi.md#webwebscraperhealthcheckhead) | **HEAD** /v1/web/health | Web scraper health check
*YahooApi* | [**yahooImageSearch**](docs/Api/YahooApi.md#yahooimagesearch) | **GET** /v1/yahoo/images | Image search
*YahooApi* | [**yahooListSupportedMarkets**](docs/Api/YahooApi.md#yahoolistsupportedmarkets) | **GET** /v1/yahoo/markets | List supported markets
*YahooApi* | [**yahooNewsSearch**](docs/Api/YahooApi.md#yahoonewssearch) | **GET** /v1/yahoo/news | News search
*YahooApi* | [**yahooSearchSuggestions**](docs/Api/YahooApi.md#yahoosearchsuggestions) | **GET** /v1/yahoo/autocomplete | Search suggestions
*YahooApi* | [**yahooVideoSearch**](docs/Api/YahooApi.md#yahoovideosearch) | **GET** /v1/yahoo/videos | Video search
*YahooApi* | [**yahooWebSearch**](docs/Api/YahooApi.md#yahoowebsearch) | **GET** /v1/yahoo/search | Web search
*YahooApi* | [**yahooYahooScraperHealthCheck**](docs/Api/YahooApi.md#yahooyahooscraperhealthcheck) | **GET** /v1/yahoo/health | Yahoo scraper health check
*YahooApi* | [**yahooYahooScraperHealthCheckHead**](docs/Api/YahooApi.md#yahooyahooscraperhealthcheckhead) | **HEAD** /v1/yahoo/health | Yahoo scraper health check
*YandexApi* | [**yandexImageSearch**](docs/Api/YandexApi.md#yandeximagesearch) | **GET** /v1/yandex/images/search | Image search
*YandexApi* | [**yandexListSupportedMarkets**](docs/Api/YandexApi.md#yandexlistsupportedmarkets) | **GET** /v1/yandex/markets | List supported markets
*YandexApi* | [**yandexReverseImageSearch**](docs/Api/YandexApi.md#yandexreverseimagesearch) | **GET** /v1/yandex/images/reverse | Reverse image search
*YandexApi* | [**yandexWebSearch**](docs/Api/YandexApi.md#yandexwebsearch) | **GET** /v1/yandex/search | Web search
*YandexApi* | [**yandexYandexScraperHealthCheck**](docs/Api/YandexApi.md#yandexyandexscraperhealthcheck) | **GET** /v1/yandex/health | Yandex scraper health check
*YandexApi* | [**yandexYandexScraperHealthCheckHead**](docs/Api/YandexApi.md#yandexyandexscraperhealthcheckhead) | **HEAD** /v1/yandex/health | Yandex scraper health check
*YouTubeApi* | [**youtubeBatchVideoDetail**](docs/Api/YouTubeApi.md#youtubebatchvideodetail) | **POST** /v1/youtube/videos/batch | Batch video detail
*YouTubeApi* | [**youtubeChannelAbout**](docs/Api/YouTubeApi.md#youtubechannelabout) | **GET** /v1/youtube/channels/{channel_id}/about | Channel about
*YouTubeApi* | [**youtubeChannelPlaylists**](docs/Api/YouTubeApi.md#youtubechannelplaylists) | **GET** /v1/youtube/channels/{channel_id}/playlists | Channel playlists
*YouTubeApi* | [**youtubeChannelShorts**](docs/Api/YouTubeApi.md#youtubechannelshorts) | **GET** /v1/youtube/channels/{channel_id}/shorts | Channel shorts
*YouTubeApi* | [**youtubeChannelStreams**](docs/Api/YouTubeApi.md#youtubechannelstreams) | **GET** /v1/youtube/channels/{channel_id}/streams | Channel streams
*YouTubeApi* | [**youtubeChannelVideos**](docs/Api/YouTubeApi.md#youtubechannelvideos) | **GET** /v1/youtube/channels/{channel_id}/videos | Channel videos
*YouTubeApi* | [**youtubeCommentReplies**](docs/Api/YouTubeApi.md#youtubecommentreplies) | **GET** /v1/youtube/videos/{video_id}/comments/{comment_id}/replies | Comment replies
*YouTubeApi* | [**youtubeCommunityPostComments**](docs/Api/YouTubeApi.md#youtubecommunitypostcomments) | **GET** /v1/youtube/posts/{post_id}/comments | Community post comments
*YouTubeApi* | [**youtubeCommunityPosts**](docs/Api/YouTubeApi.md#youtubecommunityposts) | **GET** /v1/youtube/channels/{channel_id}/community | Community posts
*YouTubeApi* | [**youtubeContentRegions**](docs/Api/YouTubeApi.md#youtubecontentregions) | **GET** /v1/youtube/regions | Content regions
*YouTubeApi* | [**youtubeGetACommunityPost**](docs/Api/YouTubeApi.md#youtubegetacommunitypost) | **GET** /v1/youtube/posts/{post_id} | Get a community post
*YouTubeApi* | [**youtubeGetAMixRadioQueue**](docs/Api/YouTubeApi.md#youtubegetamixradioqueue) | **GET** /v1/youtube/mixes/{playlist_id} | Get a mix / radio queue
*YouTubeApi* | [**youtubeGetAShort**](docs/Api/YouTubeApi.md#youtubegetashort) | **GET** /v1/youtube/shorts/{video_id} | Get a Short
*YouTubeApi* | [**youtubeGetChannelDetail**](docs/Api/YouTubeApi.md#youtubegetchanneldetail) | **GET** /v1/youtube/channels/{channel_id} | Get channel detail
*YouTubeApi* | [**youtubeGetPlaylistDetail**](docs/Api/YouTubeApi.md#youtubegetplaylistdetail) | **GET** /v1/youtube/playlists/{playlist_id} | Get playlist detail
*YouTubeApi* | [**youtubeGetVideoDetail**](docs/Api/YouTubeApi.md#youtubegetvideodetail) | **GET** /v1/youtube/videos/{video_id} | Get video detail
*YouTubeApi* | [**youtubeGuestHomeFeed**](docs/Api/YouTubeApi.md#youtubeguesthomefeed) | **GET** /v1/youtube/home | Guest home feed
*YouTubeApi* | [**youtubeKeywordSuggestions**](docs/Api/YouTubeApi.md#youtubekeywordsuggestions) | **GET** /v1/youtube/autocomplete | Keyword suggestions
*YouTubeApi* | [**youtubeListCaptionTracks**](docs/Api/YouTubeApi.md#youtubelistcaptiontracks) | **GET** /v1/youtube/videos/{video_id}/captions | List caption tracks
*YouTubeApi* | [**youtubeLiveChatMessages**](docs/Api/YouTubeApi.md#youtubelivechatmessages) | **GET** /v1/youtube/videos/{video_id}/live_chat | Live chat messages
*YouTubeApi* | [**youtubeOembedMetadata**](docs/Api/YouTubeApi.md#youtubeoembedmetadata) | **GET** /v1/youtube/oembed | oEmbed metadata
*YouTubeApi* | [**youtubePlaylistItemsPage**](docs/Api/YouTubeApi.md#youtubeplaylistitemspage) | **GET** /v1/youtube/playlists/{playlist_id}/items | Playlist items page
*YouTubeApi* | [**youtubeRelatedVideos**](docs/Api/YouTubeApi.md#youtuberelatedvideos) | **GET** /v1/youtube/videos/{video_id}/related | Related videos
*YouTubeApi* | [**youtubeResolveHandleUrlToId**](docs/Api/YouTubeApi.md#youtuberesolvehandleurltoid) | **GET** /v1/youtube/channels/resolve | Resolve handle/URL to id
*YouTubeApi* | [**youtubeSearchWithinAChannel**](docs/Api/YouTubeApi.md#youtubesearchwithinachannel) | **GET** /v1/youtube/channels/{channel_id}/search | Search within a channel
*YouTubeApi* | [**youtubeSearchYoutube**](docs/Api/YouTubeApi.md#youtubesearchyoutube) | **GET** /v1/youtube/search | Search YouTube
*YouTubeApi* | [**youtubeSearchYoutubeMusic**](docs/Api/YouTubeApi.md#youtubesearchyoutubemusic) | **GET** /v1/youtube/music/search | Search YouTube Music
*YouTubeApi* | [**youtubeShortsBySound**](docs/Api/YouTubeApi.md#youtubeshortsbysound) | **GET** /v1/youtube/shorts/by_sound/{sound_id} | Shorts by sound
*YouTubeApi* | [**youtubeStreamFormats**](docs/Api/YouTubeApi.md#youtubestreamformats) | **GET** /v1/youtube/videos/{video_id}/streams | Stream formats
*YouTubeApi* | [**youtubeSubscriberCountFast**](docs/Api/YouTubeApi.md#youtubesubscribercountfast) | **GET** /v1/youtube/channels/{channel_id}/subscriber_count | Subscriber count (fast)
*YouTubeApi* | [**youtubeSupportedMarkets**](docs/Api/YouTubeApi.md#youtubesupportedmarkets) | **GET** /v1/youtube/markets | Supported markets
*YouTubeApi* | [**youtubeTrendingShorts**](docs/Api/YouTubeApi.md#youtubetrendingshorts) | **GET** /v1/youtube/trending/shorts | Trending shorts
*YouTubeApi* | [**youtubeTrendingVideos**](docs/Api/YouTubeApi.md#youtubetrendingvideos) | **GET** /v1/youtube/trending | Trending videos
*YouTubeApi* | [**youtubeUiLanguages**](docs/Api/YouTubeApi.md#youtubeuilanguages) | **GET** /v1/youtube/languages | UI languages
*YouTubeApi* | [**youtubeVideoCategories**](docs/Api/YouTubeApi.md#youtubevideocategories) | **GET** /v1/youtube/categories | Video categories
*YouTubeApi* | [**youtubeVideoComments**](docs/Api/YouTubeApi.md#youtubevideocomments) | **GET** /v1/youtube/videos/{video_id}/comments | Video comments
*YouTubeApi* | [**youtubeVideoTranscript**](docs/Api/YouTubeApi.md#youtubevideotranscript) | **GET** /v1/youtube/videos/{video_id}/transcript | Video transcript
*YouTubeApi* | [**youtubeVideosUnderAHashtag**](docs/Api/YouTubeApi.md#youtubevideosunderahashtag) | **GET** /v1/youtube/hashtags/{tag} | Videos under a hashtag
*YouTubeApi* | [**youtubeYoutubeScraperHealthCheck**](docs/Api/YouTubeApi.md#youtubeyoutubescraperhealthcheck) | **GET** /v1/youtube/health | YouTube scraper health check
*YouTubeApi* | [**youtubeYoutubeScraperHealthCheckHead**](docs/Api/YouTubeApi.md#youtubeyoutubescraperhealthcheckhead) | **HEAD** /v1/youtube/health | YouTube scraper health check
*ZillowApi* | [**zillowGetAgentProfileListings**](docs/Api/ZillowApi.md#zillowgetagentprofilelistings) | **GET** /v1/zillow/agent | Get agent profile + listings
*ZillowApi* | [**zillowGetPropertyDetail**](docs/Api/ZillowApi.md#zillowgetpropertydetail) | **GET** /v1/zillow/property/{zpid} | Get property detail
*ZillowApi* | [**zillowGetPropertyDetailByUrl**](docs/Api/ZillowApi.md#zillowgetpropertydetailbyurl) | **GET** /v1/zillow/property | Get property detail by URL
*ZillowApi* | [**zillowListCoverageMarkets**](docs/Api/ZillowApi.md#zillowlistcoveragemarkets) | **GET** /v1/zillow/markets | List coverage markets
*ZillowApi* | [**zillowRegionAddressSuggestions**](docs/Api/ZillowApi.md#zillowregionaddresssuggestions) | **GET** /v1/zillow/autocomplete | Region/address suggestions
*ZillowApi* | [**zillowSearchProperties**](docs/Api/ZillowApi.md#zillowsearchproperties) | **GET** /v1/zillow/search | Search properties
*ZillowApi* | [**zillowZillowScraperHealthCheck**](docs/Api/ZillowApi.md#zillowzillowscraperhealthcheck) | **GET** /v1/zillow/health | Zillow scraper health check
*ZillowApi* | [**zillowZillowScraperHealthCheckHead**](docs/Api/ZillowApi.md#zillowzillowscraperhealthcheckhead) | **HEAD** /v1/zillow/health | Zillow scraper health check

## Models

- [AccountInfo](docs/Model/AccountInfo.md)
- [BillingLogListResponse](docs/Model/BillingLogListResponse.md)
- [BillingLogResponse](docs/Model/BillingLogResponse.md)
- [FilterRuleCreate](docs/Model/FilterRuleCreate.md)
- [FilterRuleDeliveryLogListResponse](docs/Model/FilterRuleDeliveryLogListResponse.md)
- [FilterRuleDeliveryLogResponse](docs/Model/FilterRuleDeliveryLogResponse.md)
- [FilterRuleListResponse](docs/Model/FilterRuleListResponse.md)
- [FilterRuleResponse](docs/Model/FilterRuleResponse.md)
- [FilterRuleUpdate](docs/Model/FilterRuleUpdate.md)
- [FilterRuleValidateRequest](docs/Model/FilterRuleValidateRequest.md)
- [FilterRuleValidateResponse](docs/Model/FilterRuleValidateResponse.md)
- [HTTPValidationError](docs/Model/HTTPValidationError.md)
- [PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse](docs/Model/PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse.md)
- [StreamMonitorCreate](docs/Model/StreamMonitorCreate.md)
- [StreamMonitorListResponse](docs/Model/StreamMonitorListResponse.md)
- [StreamMonitorResponse](docs/Model/StreamMonitorResponse.md)
- [StreamMonitorUpdate](docs/Model/StreamMonitorUpdate.md)
- [SubscriptionInfo](docs/Model/SubscriptionInfo.md)
- [TweetDeliveryLogListResponse](docs/Model/TweetDeliveryLogListResponse.md)
- [TweetDeliveryLogResponse](docs/Model/TweetDeliveryLogResponse.md)
- [ValidationError](docs/Model/ValidationError.md)
- [ValidationErrorLocInner](docs/Model/ValidationErrorLocInner.md)
- [WebhookCreate](docs/Model/WebhookCreate.md)
- [WebhookListItem](docs/Model/WebhookListItem.md)
- [WebhookListResponse](docs/Model/WebhookListResponse.md)
- [WebhookResponse](docs/Model/WebhookResponse.md)
- [WebhookTestRequest](docs/Model/WebhookTestRequest.md)
- [WebhookTestResponse](docs/Model/WebhookTestResponse.md)

## Authorization

Authentication schemes defined for the API:
### ApiKeyAuth

- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `0.1.0`
    - Package version: `0.1.0`
    - Generator version: `7.10.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`

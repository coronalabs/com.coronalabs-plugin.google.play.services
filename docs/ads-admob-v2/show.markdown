# admob.show()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, admob
> __See also__          [ads.hide()][plugin.ads-admob-v2.hide]
>								[ads.init()][plugin.ads-admob-v2.init]
>								[ads.load()][plugin.ads-admob-v2.load]
>								[ads.isLoaded()][plugin.ads-admob-v2.isLoaded]
>								[admob.*][plugin.ads-admob-v2]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

`ads.show()` begins showing ads at the specified screen location. For `"banner"` ads, calling `ads.show()` loads and displays the ad. After the banner ad loads or an error occurs, the `"adsRequest"` listener is called.

For `"interstitial"` ads, you can either call `ads.show()` to load and show the ad or call [ads.load()][plugin.ads-admob-v2.load] to preload the ad. For preloaded ads, you can call [ads.isLoaded()][plugin.ads-admob-v2.isLoaded] to verify that the ad has been loaded and is ready to show and then call `ads.show()` to show the preloaded ad.  If `ads.show()` is called after `ads.load()` then the listener will only get a `"shown"` event.

## Syntax

	ads.show( adUnitType [, params] )

##### adUnitType ~^(required)^~
_[String][api.type.String]._ The type of ad to show. AdMob supports either `"banner"` or `"interstitial"`.

##### params ~^(optional)^~
_[Table][api.type.Table]._ A table that specifies properties for the ad request — see the next section for details.


## Parameter Reference

The `params` table can include properties for the ad request.

##### x ~^(optional)^~
_[Number][api.type.Number]._ The left position of the banner ad. Defaults to `0`.

##### y ~^(optional)^~
_[Number][api.type.Number]._ The top position of the banner ad. Defaults to `0`.

##### targetingOptions ~^(optional)^~
_[Table][api.type.Table]._ An optional table of targeting parameters for the ad request. Valid <nobr>key-value</nobr> pairs include:

* `tagForChildDirectedTreatment` &mdash; [Boolean][api.type.Boolean] value indicating if the ad request should be <nobr>child-directed</nobr>.

##### appId ~^(optional)^~
_[String][api.type.String]._ The app ID. If this is not specified, the value provided to [ads.init()][plugin.ads-admob-v2.init] is used instead.

##### testMode ~^(optional)^~
_[Boolean][api.type.Boolean]._ Set to `true` to enable test ads and `false` for regular ads.

## Example

``````lua
local ads = require( "ads" )

local function adListener( event )
	if ( event.isError ) then
		-- Failed to receive an ad
	end
end
 
ads.init( "admob", "myAppId", adListener )

-- Optional table containing targeting parameters
local targetingParams = { tagForChildDirectedTreatment = true }

ads.show( "banner", { x=0, y=0, targetingOptions=targetingParams, appId="otherAppId" } )
``````
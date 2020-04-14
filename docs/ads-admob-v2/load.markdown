# admob.load()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, admob
> __See also__          [ads.show()][plugin.ads-admob-v2.show]
>								[ads.isLoaded()][plugin.ads-admob-v2.isLoaded]
>								[admob.*][plugin.ads-admob-v2]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

Preloads an ad. Only works with the string `"interstitial"` for the first argument. You can also call [ads.isLoaded()][plugin.ads-admob-v2.isLoaded] to verify that the ad has been loaded and [ads.show()][plugin.ads-admob-v2.show] to show it.


## Syntax

	ads.load( adUnitType [, params] )

##### adUnitType ~^(required)^~
_[String][api.type.String]._ The type of ad to show. AdMob supports `"interstitial"` for this command.

##### params ~^(optional)^~
_[Table][api.type.Table]._ A table that specifies properties for the ad request — see the next section for details.


## Parameter Reference

The `params` table can include properties for the ad request.

##### appId ~^(optional)^~
_[String][api.type.String]._ The app ID. If this is not specified, the value provided to [ads.init()][plugin.ads-admob-v2.init] is used instead.

##### testMode ~^(optional)^~
_[Boolean][api.type.Boolean]._ Set to `true` to enable test ads and `false` for regular ads. At this time, test mode only works on Android devices and in the Xcode Simulator. Test ads do not work on iOS devices.


## Example

``````lua
local ads = require( "ads" )

local function adListener( event )
	if ( event.isError ) then
		-- Failed to receive an ad
	else
		ads.show( "interstitial", { x=0, y=0, appId="otherAppId" } )
	end

end
 
ads.init( "admob", "myAppId", adListener )

ads.load( "interstitial", { appId="otherAppId", testMode=false } )
``````
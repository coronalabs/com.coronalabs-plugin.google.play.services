# admob.*

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [CoronaProvider][api.type.CoronaProvider]
> __Library__           [ads.*][api.library.ads]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, admob
> __Platforms__			Android, iOS
> --------------------- ------------------------------------------------------------------------------------------


## Overview

The AdMob plugin offers easy integration of AdMob ads using the [ads][api.library.ads] library and [ads.init()][plugin.ads-admob-v2.init].


## Syntax

	local ads = require( "ads" )

## Functions

#### [ads.init()][plugin.ads-admob-v2.init]

#### [ads.show()][plugin.ads-admob-v2.show]

#### [ads.hide()][plugin.ads-admob-v2.hide]

#### [ads.height()][plugin.ads-admob-v2.height]

#### [ads.isLoaded()][plugin.ads-admob-v2.isLoaded]

#### [ads.load()][plugin.ads-admob-v2.load]


## Events

#### [adsRequest][plugin.ads-admob-v2.event.adsRequest]


## Project Settings

To use this plugin, add an entry into the `plugins` table of `build.settings`. When added, the build server will integrate the plugin during the build phase.

``````lua
settings =
{
	plugins =
	{
		["plugin.google.play.services"] =
		{
			publisherId = "com.coronalabs",
			supportedPlatforms = { iphone=true, android=true }
		},
	},		
}
``````

<div class="guide-notebox">
<div class="notebox-title">Note</div>

For Android, the following permissions/features are automatically added when using this plugin:

``````lua
	android =
	{
		usesPermissions =
		{
			"android.permission.INTERNET",
			"android.permission.ACCESS_NETWORK_STATE"
		},
	},
``````

</div>

## Support

* [http://www.google.com/ads/admob/](http://www.google.com/ads/admob/)
* [Corona Forums](http://forums.coronalabs.com/forum/545-monetization-in-app-purchases-ads-etc/)

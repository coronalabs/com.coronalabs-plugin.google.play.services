# admob.init()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, admob
> __See also__          [ads.show()][plugin.ads-admob-v2.show]
>								[ads.load()][plugin.ads-admob-v2.load]
>								[admob.*][plugin.ads-admob-v2]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

`ads.init()` initializes the Corona `ads` library by specifying the name of the ad network service provider and the app identifier.

Once the `ads` library is initialized, you can request an ad using [ads.show()][plugin.ads-admob-v2.show] or [ads.load()][plugin.ads-admob-v2.load].


## Syntax

	ads.init( providerName, appId [, adListener] )

##### providerName ~^(required)^~
_[String][api.type.String]._ String value for the provider name. For AdMob, use `"admob"`.

##### appId ~^(required)^~
_[String][api.type.String]._ String containing the app ID.

##### adListener ~^(optional)^~
_[Listener][api.type.Listener]._ Listener function that will receive [adsRequest][plugin.ads-admob-v2.event.adsRequest] events.

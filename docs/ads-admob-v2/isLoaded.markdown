# admob.isLoaded()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      [Boolean][api.type.Boolean]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, admob
> __See also__          [ads.show()][plugin.ads-admob-v2.show]
>								[admob.*][plugin.ads-admob-v2]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

Checks to see if the specified ad type is already loaded. Currently, this only works with the string `"interstitial"` for the first argument.

This can be called after calling [ads.load()][plugin.ads-admob-v2.load] to determine if the ad is loaded and ready to be displayed. Returns `true` if the ad is loaded/ready, otherwise returns `false`.


## Syntax

	ads.isLoaded( "interstitial" )

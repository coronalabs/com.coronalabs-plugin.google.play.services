# admob.hide()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, admob
> __See also__          [ads.show()][plugin.ads-admob-v2.show]
>								[admob.*][plugin.ads-admob-v2]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

Removes the currently showing banner ad from the screen and prevents new ads from being retrieved until [ads.show()][plugin.ads-admob-v2.show] is called again. If you wish to use ads from another [provider][api.library.ads] in different scenes of an app, you should hide the current ads before initializing ads for the new provider. Does not work with interstitial ads.


## Syntax

	ads.hide()

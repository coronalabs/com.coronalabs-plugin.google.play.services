# admob.height()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, admob
> __See also__          [ads.show()][plugin.ads-admob-v2.show]
>								[admob.*][plugin.ads-admob-v2]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

Gets the height of the banner ad in content coordinates. This will only return the correct result after calling [ads.show()][plugin.ads-admob-v2.show]. After the device has been rotated, you must call [ads.show()][plugin.ads-admob-v2.show] again to get the new correct height.

## Syntax

	ads.height()

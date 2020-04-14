# event.phase

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Event__             [adsRequest][plugin.ads-admob-v2.event.adsRequest]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, admob, adsRequest, phase
> __See also__			[adsRequest][plugin.ads-admob-v2.event.adsRequest]
>						[admob.*][plugin.ads-admob-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

[String][api.type.String] value indicating the phase of the [adsRequest][plugin.ads-admob-v2.event.adsRequest] event. Possible values include:

* `"loaded"` &mdash; Indicates that an ad has been loaded via [ads.load()][plugin.ads-admob-v2.load].

* `"shown"` &mdash; Indicates that an ad has been shown on the screen via [ads.show()][plugin.ads-admob-v2.show].

* `"refresh"` &mdash; Indicates that a new ad has been received for banners.
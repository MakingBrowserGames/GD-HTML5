[![NPM version](https://badge.fury.io/js/badge-list.svg)](http://badge.fury.io/js/badge-list)
[![Built with Grunt](https://cdn.gruntjs.com/builtwith.svg)](http://gruntjs.com/)
[![GitHub version](https://badge.fury.io/gh/boennemann%2Fbadges.svg)](http://badge.fury.io/gh/boennemann%2Fbadges)
[![Open Source Love](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://github.com/ellerbrock/open-source-badge/)


# Gamedistribution.com HTML5 API
This is the documentation of the "Gamedistribution.com HTML5 API" project.

Gamedistribution.com is the biggest broker of high quality, cross-platform games. We connect the best game developers to the biggest publishers.

Running into any issues? Check out the F.A.Q. within the Wiki of the github repository before mailing to <a href="support@gamedistribution.com" target="_blank">support@gamedistribution.com</a>

## About the API
The API should be integrated within HTML5 games by simple import or loading the CDN. An example for CDN integration is available within the 'index.html' at the root of the project folder.

```
import gdApi from 'gamedistribution-gdApi';
```

Specific information of its usage can be found at the <a href="https://github.com/GameDistribution/GD-HTML5/wiki" target="_blank">wiki</a>.

## Repository
The API is maintained on a public github repository.
<a href="https://github.com/GameDistribution/GD-HTML5" target="_blank">https://github.com/GameDistribution/GD-HTML5</a>

## Deployment
Deployment of the API to production environments and npmjs.com is done through TeamCity.

## Installation
Install the following programs:
* [NodeJS LTS](https://nodejs.org/).
* [Grunt](http://gruntjs.com/).

Pull in the rest of the requirements using npm:
```
npm install
```

Setup a local node server, watch changes and update your browser view automatically:
```
grunt
```

Make a production build:
```
grunt build
```

## Debugging
Games, which include the API, can be easily debugged by calling the following from a browser developer console:
```
gdApi.openConsole();
```

## Events
### API EVENTS
The API events should be used by developers to start or pause their game or handling critical errors. Unless the errors are ad related, then they could hook into the AD_ERROR event, however; the API should gracefully fail, so this should not be needed.
| Event | Description |
| --- | --- |
| API_READY | When the API is ready. |
| API_ERROR | When the API has hit a critical error. |
| API_GAME_DATA_READY | When game data is returned. |
| API_GAME_START | When the game should start. |
| API_GAME_PAUSE | When the game should pause. |

### IMA SDK EVENTS
The SDK events are custom ads for handling any thing related to the IMA SDK itself.
| Event | Description |
| --- | --- |
| AD_SDK_LOADER_READY | When the adsLoader instance is ready to create an adsManager instance |
| AD_SDK_MANAGER_READY | When the adsManager instance is ready with ads. |
| AD_SDK_REQUEST_ADS | When new ads are requested. |
| AD_SDK_ERROR | When the SDK hits a critical error. |
| AD_SDK_FINISHED | When the SDK is finished running the ad. |
| AD_CANCELED | When the ad is cancelled or stopped because its done running an ad. |
| AD_SAFETY_TIMER | When the safety timer is cleared. We run this timer to make sure the SDK and ads do not stop us from starting the game after, whenever there is a weird error. |

### AD EVENTS
The Gamedistribution.com API uses the IMA SDK for loading ads. All events of this SDK are also available to the developer.
https://developers.google.com/interactive-media-ads/docs/sdks/html5/

| Event | Description |
| --- | --- |
| AD_ERROR | When the ad it self has an error. | 
| AD_BREAK_READY | Fired when an ad rule or a VMAP ad break would have played if autoPlayAdBreaks is false. |
| AD_METADATA | Fired when an ads list is loaded. |
| ALL_ADS_COMPLETED | Fired when the ads manager is done playing all the ads. |
| CLICK | Fired when the ad is clicked. |
| COMPLETE | Fired when the ad completes playing. |
| CONTENT_PAUSE_REQUESTED | Fired when content should be paused. This usually happens right before an ad is about to cover the content. |
| CONTENT_RESUME_REQUESTED | Fired when content should be resumed. This usually happens when an ad finishes or collapses. |
| DURATION_CHANGE | Fired when the ad's duration changes. |
| FIRST_QUARTILE | Fired when the ad playhead crosses first quartile. |
| IMPRESSION | Fired when the impression URL has been pinged. |
| INTERACTION | Fired when an ad triggers the interaction callback. Ad interactions contain an interaction ID string in the ad data. |
| LINEAR_CHANGED | Fired when the displayed ad changes from linear to nonlinear, or vice versa. |
| LOADED | Fired when ad data is available. |
| LOG | Fired when a non-fatal error is encountered. The user need not take any action since the SDK will continue with the same or next ad playback depending on the error situation. |
| MIDPOINT | Fired when the ad playhead crosses midpoint. |
| PAUSED | Fired when the ad is paused. |
| RESUMED | Fired when the ad is resumed. |
| SKIPPABLE_STATE_CHANGED | Fired when the displayed ads skippable state is changed. |
| SKIPPED | Fired when the ad is skipped by the user. |
| STARTED | Fired when the ad starts playing. |
| THIRD_QUARTILE | Fired when the ad playhead crosses third quartile. |
| USER_CLOSE | Fired when the ad is closed by the user. |
| VOLUME_CHANGED | Fired when the ad volume has changed. |
| VOLUME_MUTED | Fired when the ad volume has been muted. |



	

	

	

	

	

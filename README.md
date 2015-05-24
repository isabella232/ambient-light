# Ambient Light Mapbox GL iOS Demo

A [Mapbox GL for iOS](https://github.com/mapbox/mapbox-gl-native) demo app that demonstrates ambient light-based map styling.

![Would be nice to live in London, wouldn't it.](https://cloud.githubusercontent.com/assets/1198851/7789421/78569c38-0214-11e5-8cc7-9891b7507a5a.png)

## Getting started

1.  Clone or [download](https://github.com/friedbunny/ambient-light/archive/master.zip) this repository
1. Run `pod install` to download the Mapbox GL library via [Cocoapods](https://cocoapods.org)
1. Open `ambient-light.xcworkspace` in Xcode
1. Insert your [Mapbox access token](https://www.mapbox.com/developers/api/#access-tokens) into Map View’s Attributes Inspector panel in Interface Builder: ![Interface Builder has lots of names for things that you'll never know about](https://cloud.githubusercontent.com/assets/1198851/7789419/5e5c002a-0214-11e5-8315-6617fb3d47c5.png)
1. Build amazing cartographic things

## Detecting ambient light

This is a bit of a lie: Apple does not expose any direct ambient light sensing API to developers, so **this demo uses screen brightness as a proxy**.

This relies on the user having auto brightness enabled, which isn’t always a given (and there’s no easy way to detect if that’s on, either).

Generally this technique works well and is the same that’s used in [Tweetbot](http://tapbots.com/tweetbot/).

## How the UI works

The slider controls the screen brightness threshold at which the map will change styles — e.g., farther left will switch to the dark style at a lower screen brightness. 

My preferred threshold is about 35%, or somewhat left of center.

## Does not work in simulator

This does not really work in the simulator as brightness is hardcoded to 50%, but you can still drag the slider to change styles.

## Need help?

If you haven’t already, read the [official project overview from Mapbox](https://www.mapbox.com/mapbox-gl-ios/) and have a look at the [API reference](https://www.mapbox.com/mapbox-gl-ios/api/). The [Mapbox tag on Stack Overflow](http://stackoverflow.com/questions/tagged/mapbox) is a great place to ask questions (that are often answered by Mapboxers). If you’re really stumped, Mapbox also offers [official support via email](https://www.mapbox.com/help/).

## Found a bug?

If you’ve found a bug in the Mapbox GL library, please take a bit to [report it at the main Mapbox GL Native project](https://github.com/mapbox/mapbox-gl-native/issues).
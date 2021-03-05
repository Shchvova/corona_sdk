### Version 4.26.2 Android/4.26.1 iOS (5th March 2021)
- Added method `appTrackingAuthorizationStatus`: returns integer of user consent (effective only on iOS, no-op on Android)
- Added method `updateConversionValue`: sets iOS Conversion value (no-op on Android)
- Added `needsCost` value of `create` method of `Adjust` along with `costType`, `needsCost` and `costAmount` fields in `attribution` data.

### Version 4.23.1 (29th September 2020)
#### Fixed
- Fixed duplicate `ADJUrlStrategy` symbol error.

#### Native SDKs
- [iOS@v4.23.2][ios_sdk_v4.23.2]
- [Android@v4.24.1][android_sdk_v4.24.1]

---

### Version 4.23.0 (8th September 2020)
#### Added
- Added subscription tracking feature.
- Added communication with SKAdNetwork framework by default on iOS 14.
- Added method `handleSkAdNetwork` key handling to configuration map to switch off default communication with SKAdNetwork framework in iOS 14.
- Added wrapper method `requestTrackingAuthorizationWithCompletionHandler` to `Adjust` to allow asking for user's consent to be tracked in iOS 14 and immediate propagation of user's choice to backend.
- Added handling of new iAd framework error codes introduced in iOS 14.
- Added sending of value of user's consent to be tracked with each package.
- Added `urlStrategy` key handling to configuration map to allow selection of URL strategy for specific market.

#### Native SDKs
- [iOS@v4.23.0][ios_sdk_v4.23.0]
- [Android@v4.24.0][android_sdk_v4.24.0]

---

### Version 4.21.0 (25th March 2020)
#### Added
- Added support for signature library as a plugin.
- Added more aggressive sending retry logic for install session package.
- Added additional parameters to `ad_revenue` package payload.

#### Native SDKs
- [iOS@v4.21.0][ios_sdk_v4.21.0]
- [Android@v4.21.0][android_sdk_v4.21.0]

---

### Version 4.20.0 (9th February 2020)
#### Added
- Added `disableThirdPartySharing` method to `Adjust` interface to allow disabling of data sharing with third parties outside of Adjust ecosystem.
- Added external device ID support.

#### Fixed
- Fixed potential events submission after Lua state has already been destroyed (thanks to @Shchvova).

#### Native SDKs
- [iOS@v4.20.0][ios_sdk_v4.20.0]
- [Android@v4.20.0][android_sdk_v4.20.0]

---

### Version 4.18.0 (4th July 2019)
#### Added
- Added `trackAdRevenue` method to `Adjust` interface to allow tracking of ad revenue. With this release added support for `MoPub` ad revenue tracking.
- Added reading of Facebook anonymous ID if available on iOS platform.

#### Native SDKs
- [iOS@v4.18.0][ios_sdk_v4.18.0]
- [Android@v4.18.0][android_sdk_v4.18.0]

---

### Version 4.17.0 (22nd January 2019)
#### Added
- Added `getSdkVersion` method to `Adjust` interface to obtain current SDK version string.
- Added ability to pass `callbackId` value through `trackEvent` method of `Adjust` interface, for users to set custom ID on event object which will later be reported in event success/failure callbacks.
- Added `callbackId` field to event tracking success callback object.
- Added `callbackId` field to event tracking failure callback object.

#### Changed
- `readMobileEquipmentIdentity` value of `create` method of `Adjust` interface is deprecated.
- SDK will now fire attribution request each time upon session tracking finished in case it lacks attribution info.

#### Native SDKs
- [iOS@v4.17.1][ios_sdk_v4.17.1]
- [Android@v4.17.0][android_sdk_v4.17.0]

---

### Version 4.14.0 (16th July 2018)
#### Added
- Added deep link caching in case `appWillOpenUrl` method is called before SDK is initialised.

#### Changed
- Updated the way how iOS plugin handles push tokens from Corona interface - they are now being passed directly as strings to native iOS SDK.

#### Native SDKs
- [iOS@v4.14.1][ios_sdk_v4.14.1]
- [Android@v4.14.0][android_sdk_v4.14.0]

---

### Version 4.13.1 (18th May 2018)
#### Fixed
- Added null check for `CoronaRuntimeTaskDispatcher` (https://github.com/adjust/corona_sdk/issues/6).

#### Native SDKs
- [iOS@v4.13.0][ios_sdk_v4.13.0]
- [Android@v4.13.0][android_sdk_v4.13.0]

---

### Version 4.13.0 (16th May 2018)
#### Added
- Added `gdprForgetMe()` method to Adjust interface to enable possibility for user to be forgotten in accordance with GDPR law.

#### Native SDKs
- [iOS@v4.13.0][ios_sdk_v4.13.0]
- [Android@v4.13.0][android_sdk_v4.13.0]

---

### Version 4.12.2 (12th March 2018)
#### Native changes
- Updated iOS SDK to `v4.12.3`.
- Updated Android SDK to `v4.12.4`.

#### Native SDKs
- [iOS@v4.12.3][ios_sdk_v4.12.3]
- [Android@v4.12.4][android_sdk_v4.12.4]

---

### Version 4.12.1 (1st February 2018)
#### Native changes
- https://github.com/adjust/android_sdk/blob/master/CHANGELOG.md#version-4121-31st-january-2018

#### Native SDKs
- [iOS@v4.12.1][ios_sdk_v4.12.1]
- [Android@v4.12.1][android_sdk_v4.12.1]

---

### Version 4.12.0 (22nd December 2017)
#### Added
- Initial release of Corona SDK. Supported platforms: `iOS` and `Android`.

#### Native SDKs
- [iOS@v4.12.1][ios_sdk_v4.12.1]
- [Android@v4.12.0][android_sdk_v4.12.0]

[ios_sdk_v4.12.1]: https://github.com/adjust/ios_sdk/tree/v4.12.1
[ios_sdk_v4.12.3]: https://github.com/adjust/ios_sdk/tree/v4.12.3
[ios_sdk_v4.13.0]: https://github.com/adjust/ios_sdk/tree/v4.13.0
[ios_sdk_v4.14.1]: https://github.com/adjust/ios_sdk/tree/v4.14.1
[ios_sdk_v4.17.1]: https://github.com/adjust/ios_sdk/tree/v4.17.1
[ios_sdk_v4.18.0]: https://github.com/adjust/ios_sdk/tree/v4.18.0
[ios_sdk_v4.20.0]: https://github.com/adjust/ios_sdk/tree/v4.20.0
[ios_sdk_v4.21.0]: https://github.com/adjust/ios_sdk/tree/v4.21.0
[ios_sdk_v4.23.0]: https://github.com/adjust/ios_sdk/tree/v4.23.0
[ios_sdk_v4.23.2]: https://github.com/adjust/ios_sdk/tree/v4.23.2

[android_sdk_v4.12.0]: https://github.com/adjust/android_sdk/tree/v4.12.0
[android_sdk_v4.12.1]: https://github.com/adjust/android_sdk/tree/v4.12.1
[android_sdk_v4.13.0]: https://github.com/adjust/android_sdk/tree/v4.13.0
[android_sdk_v4.14.0]: https://github.com/adjust/android_sdk/tree/v4.14.0
[android_sdk_v4.17.0]: https://github.com/adjust/android_sdk/tree/v4.17.0
[android_sdk_v4.18.0]: https://github.com/adjust/android_sdk/tree/v4.18.0
[android_sdk_v4.20.0]: https://github.com/adjust/android_sdk/tree/v4.20.0
[android_sdk_v4.21.0]: https://github.com/adjust/android_sdk/tree/v4.21.0
[android_sdk_v4.24.0]: https://github.com/adjust/android_sdk/tree/v4.24.0
[android_sdk_v4.24.1]: https://github.com/adjust/android_sdk/tree/v4.24.1

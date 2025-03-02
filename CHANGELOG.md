#

## [v2.0.0](https://github.com/mixpanel/mixpanel-flutter/tree/v2.0.0) (2022-09-09)

### BREAKING CHANGE: 
This major release removes all remaining calls to Mixpanel's `/decide` API endpoint. The main effect of this is that the SDK no longer fetches the remote status of your [project's "Automatically collect common mobile events" setting](https://help.mixpanel.com/hc/en-us/articles/115004596186#enable-or-disable-common-mobile-events). From this version forward, automatic event tracking can only be controlled by the, now required, parameter `trackAutomaticEvents`. Upon upgrading, existing implementations will need to add this parameter to their Mixpanel initializer calls. 

```
import 'package:mixpanel_flutter/mixpanel_flutter.dart';

class MixpanelManager {
  static Mixpanel? _instance;

  static Future<Mixpanel> init() async {
    if (_instance == null) {
      _instance = await Mixpanel.init("YOUR_PROJECT_TOKEN", trackAutomaticEvents: true);
    }
    return _instance!;
  }
}

```

### Enhancements

- add param 'trackAutomaticEvents' to 'init' [\#86](https://github.com/mixpanel/mixpanel-flutter/pull/86)

#

## [v1.6.0](https://github.com/mixpanel/mixpanel-flutter/tree/v1.6.0) (2022-06-24)

### Enhancements

- bump versions to get millisecond precision for event time property [\#82](https://github.com/mixpanel/mixpanel-flutter/pull/82)

#

## [v1.5.1](https://github.com/mixpanel/mixpanel-flutter/tree/v1.5.1) (2022-05-20)

### Enhancements

- bump versions to remove survey [\#79](https://github.com/mixpanel/mixpanel-flutter/pull/79)

#

## [v1.5.0](https://github.com/mixpanel/mixpanel-flutter/tree/v1.5.0) (2022-05-09)

### Enhancements

- add config for web init and setServerURL for web [\#75](https://github.com/mixpanel/mixpanel-flutter/pull/75)
- feat: support `DateTime` and `Uri` [\#66](https://github.com/mixpanel/mixpanel-flutter/pull/66)
- fix: Make `flush` method asynchronous [\#64](https://github.com/mixpanel/mixpanel-flutter/pull/64)

#

## [v1.4.8](https://github.com/mixpanel/mixpanel-flutter/tree/v1.4.8) (2022-05-06)

#

## [v1.4.7](https://github.com/mixpanel/mixpanel-flutter/tree/v1.4.7) (2022-05-06)

#

## [v1.4.6](https://github.com/mixpanel/mixpanel-flutter/tree/v1.4.6) (2022-04-11)

### Enhancements

- bump iOS SDK version to 3.1.7 and Android to 6.1.1 [\#69](https://github.com/mixpanel/mixpanel-flutter/pull/69)

### Fixes

- Registering non-string super props in init fails [\#51](https://github.com/mixpanel/mixpanel-flutter/issues/51)

#

## [v1.4.5](https://github.com/mixpanel/mixpanel-flutter/tree/v1.4.5) (2022-02-11)

### Enhancements

- bump iOS SDK version to 3.1.4 [\#61](https://github.com/mixpanel/mixpanel-flutter/pull/61)

### Fixes

- Fix registering non-string super props in init fails [\#62](https://github.com/mixpanel/mixpanel-flutter/pull/62)
- Fix several misspellings of "Mixpanel" [\#60](https://github.com/mixpanel/mixpanel-flutter/pull/60)
- Fix backward ordering of 'alias\(\)' parameters on Android. [\#58](https://github.com/mixpanel/mixpanel-flutter/pull/58)

#

## [v1.4.4](https://github.com/mixpanel/mixpanel-flutter/tree/v1.4.4) (2022-01-26)

### Fixes

- Bump iOS SDK depedency to v3.1.2 [\#52](https://github.com/mixpanel/mixpanel-flutter/pull/52)

#

## [v1.4.3](https://github.com/mixpanel/mixpanel-flutter/tree/v1.4.3) (2022-01-19)
## Caution: Please DO NOT use this build! In this version, we have a bug in iOS that event names with & or % will be rejected by the server. We recommend you update to 1.4.4 or above.

### Fixes

- Now First App Open will display 'flutter' as property value for 'Mixpanel Library'  in iOS [\#49](https://github.com/mixpanel/mixpanel-flutter/pull/49)

#

## [v1.4.2](https://github.com/mixpanel/mixpanel-flutter/tree/v1.4.2) (2022-01-05)


**Merged pull requests:**

- bump Mixpanel native SDK version to iOS 3.0.0, Android 6.0.0 [\#46](https://github.com/mixpanel/mixpanel-flutter/pull/44)
- register super properties on Mixpanel.init for iOS [\#46](https://github.com/mixpanel/mixpanel-flutter/pull/46)
- fix nested dictionary not being able to tracked properly in iOS [\#43](https://github.com/mixpanel/mixpanel-flutter/pull/43)

#

## [v1.4.1](https://github.com/mixpanel/mixpanel-flutter/tree/v1.4.1) (2021-12-04)

**Merged pull requests:**

- Some lint fixes [\#40](https://github.com/mixpanel/mixpanel-flutter/pull/40)

#

## [v1.4.0](https://github.com/mixpanel/mixpanel-flutter/tree/v1.4.0) (2021-12-02)

### Enhancements

- Add web support [\#35](https://github.com/mixpanel/mixpanel-flutter/pull/35)
Please add the following snippet to your web/index.html inside <head></head> in your Flutter project.

<script src="./assets/packages/mixpanel_flutter/assets/mixpanel.js"></script>

#

## [v1.3.1](https://github.com/mixpanel/mixpanel-flutter/tree/v1.3.1) (2021-09-25)

### Enhancements

- Migrate from JCenter [\#22](https://github.com/mixpanel/mixpanel-flutter/issues/22)

**Merged pull requests:**

- Bump native SDK dependencies [\#29](https://github.com/mixpanel/mixpanel-flutter/pull/29)

#

## [v1.3.0](https://github.com/mixpanel/mixpanel-flutter/tree/v1.3.0) (2021-09-21)

### Enhancements

- change the name 'properties' to 'superProperties' in init [\#28](https://github.com/mixpanel/mixpanel-flutter/pull/28)
- Add superProperties on initialize [\#14](https://github.com/mixpanel/mixpanel-flutter/pull/14)

**Merged pull requests:**

- Remove jCenter [\#24](https://github.com/mixpanel/mixpanel-flutter/pull/24)

#

## [v1.2.1](https://github.com/mixpanel/mixpanel-flutter/tree/v1.2.1) (2021-07-19)

### Fixes

- Fix the bool value being tracked as Int [\#21](https://github.com/mixpanel/mixpanel-flutter/pull/21)

#

## [v1.2.0](https://github.com/mixpanel/mixpanel-flutter/tree/v1.2.0) (2021-07-01)

### Enhancements

- Add API `setUseIpAddressForGeolocation` [\#18](https://github.com/mixpanel/mixpanel-flutter/pull/18)

## 1.1.0
* Add support for Null Safety! Thanks @incendial for contributing a PR for this. 🙏

## 1.0.1
* Improve docs

## 1.0.0
* 🚀 This is our first release!  🎉🎉🎉
    Report issues or give us any feedback is appreciated!
* [integration guide](https://developer.mixpanel.com/docs/flutter)
* [full API reference](https://mixpanel.github.io/mixpanel-flutter)


































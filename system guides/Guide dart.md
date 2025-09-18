# Dart Guide
## Clean flutter cache/build
```bash
flutter clean
flutter pub get
```


## Check for updates
```bash
flutter upgrade
flutter pub upgrade --major-versions
dart run dependency_validator
```

For iOS only:
from ios:
```bash
rm -rf Pods Podfile.lock .symlinks Flutter/Flutter.podspec
flutter clean                                        
flutter pub get
pod install --repo-update
```

If unknown error
- check that systems/platforms are updated (see below)

----
pod deintegrate
gem install cocoapods
pod update


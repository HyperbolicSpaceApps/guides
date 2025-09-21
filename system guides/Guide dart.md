# Dart Guide
## Clean flutter cache/build
```zsh
flutter clean
flutter pub get
```


## Check for updates
```zsh
flutter upgrade
flutter pub upgrade --major-versions
dart run dependency_validator
```

For iOS only:
```zsh
cd ios
rm -rf Pods Podfile.lock .symlinks Flutter/Flutter.podspec
flutter clean                                        
flutter pub get
pod install --repo-update
cd ..
```

If unknown error, check that systems/platforms are updated:

```zsh
pod deintegrate
gem install cocoapods
pod update
```

# Android Screenshots Guide
Can be done after release

- take screenshot from physical device
- move it to icons/screenshots/ios for the record
- log in to Google Play Console
- “Grow” “Store presence” “Default store listing.” Scroll down to “Phone”

# iOS Screenshots Guide
Has to be done during release

- open Simulator app
- File -> Open Emulator -> iPhone 11 Pro Max/iPad Pro 13-inch (M4)
    - if needed to add another, check requirements from app store connect + https://iosref.com/res
- select device in vs code (lower right corner)
- flutter run --dart-define-from-file=lib/api-keys.json
- Take a screenshot (upper right of emulator window) -> move it from Desktop to folder icons/screenshots/ios for the record
- upload during release of new version (see guide to release)

Requirements here: https://developer.apple.com/help/app-store-connect/reference/screenshot-specifications/
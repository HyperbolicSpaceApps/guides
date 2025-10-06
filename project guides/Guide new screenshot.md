# Android Screenshots Guide
Can be done after release

- take screenshot from physical device
- save them in temp file
- open with kolour paint and resize (required: 10-inch tablet sizes)
    - image -> resize -> smooth scale / keep aspect ratio / width = 1640
- log in to Google Play Console
    - Grow users: Store presence → Store listing → Edit → Graphics

# iOS Screenshots Guide
Following has to be done before release

- open Simulator app
- File -> Open Emulator -> iPhone 11 Pro Max/iPad Pro 13-inch (M4)
    - if needed to add another, check requirements from app store connect + https://iosref.com/res
- select device in vs code (lower right corner)
- flutter run --dart-define-from-file=lib/api-keys.json
- Take a screenshot (upper right of emulator window) -> move it from Desktop to folder icons/screenshots/ios for the record
- upload during release of new version (see guide to release)

Requirements here: https://developer.apple.com/help/app-store-connect/reference/screenshot-specifications/
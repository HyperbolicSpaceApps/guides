# Release Process Guide

## Before Release

1. Update the version number in `pubspec.yaml`. If unsure, check in Google Play Console's App Bundle Explorer
2. Update the release notes in `roadmap.md`.
5. If new feature, see guide to add screenshot.
6. Check for flutter/package updates (see Guide dart.md)
7. Perform Git operations (see Guide git.md).
8. Test run
```zsh
flutter run --dart-define-from-file=lib/api-keys.json
```


## Android Release Process

1. **Build the app bundle**
```zsh
flutter build appbundle --dart-define-from-file=lib/api-keys.json
```

2. **Google Play Console**
    - Navigate to Test and release -> App Bundle Explorer and upload the new version of the app. It is stored in PROJECT_APP/build/app/outputs/bundle/release/app-release.aab
    - Under Testing -> Open Testing, click **Create New Release**. Save and send changes for review.
    - In the **Manage Release** section, scroll down to **Release Notes**:
        - Edit the release details.
        - Copy and paste the release notes (maximum 500 characters).
    - Once approved, do the same from Production

## iOS Release Process


1. **Build the app ipa**
    ```zsh
    flutter build ipa --dart-define-from-file=lib/api-keys.json
    ```

2. **Open the Runner to validate and distribute**
    ```zsh
    open build/ios/archive/Runner.xcarchive
    ```

    - Validate the app.
    - Distribute the app via **App Store Connect**

3. **App Store Connect**
    - **In the TestFlight tab**
        - Check the status and fill out missing compliance details if needed.
    - **In the Distribution tab**
        - Click the **+** sign under **iOS App**, fill out the release version, release notes, and notes to reviewers.
        - Save and submit the release for review.

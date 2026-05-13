### New icons guide

If new icon entirely, start by saving it in assets/icons as .svg

```zsh
./svg_to_png.zsh ../from_zero_to_tarot_app/assets/icons/pentacle.svg "#e7d7c8" "#010101" 512 
./svg_to_png.zsh ../from_zero_to_tarot_app/assets/icons/pentacle.svg "#e7d7c8" "#010101" 512 --splash
./svg_to_png.zsh ../from_zero_to_tarot_app/assets/icons/pentacle.svg "#e7d7c8" "#010101" 512 --feature
```

- if needed, replace hexa for background/foreground colors in commands above
    - if so, update also pubspec.yaml in flutter_launcher_icons and flutter_native_splash
- copy icon.png, icon-transparent.png and splash-icon.png from generated_icons into assets/icons
- note: feature_graphic.png is only used in Google Play Store listing (see below)

```zsh
dart run flutter_launcher_icons
dart run flutter_native_splash:create
```


## Android Specifics

Upload manually icon.png and feature_graphic.png in Play Console:
Grow users: Store presence → Store listing → Edit → Graphics

## iOS Specifics

Nothing else to do.
# Studio/gradle Guide

## Open Android Studio
```zsh
cd dev/android-studio/bin/
./studio
```

## Studio/gradle Upgrades

- wait until background tasks are done (bottom bar: indexing, etc)
- from settings (upper right corner): install new android studio version (may be several)
- run AGP Upgrade assistant (from Tools)

## Refresh dependencies: 

```zsh
cd android
./gradlew --refresh-dependencies
```

## Clean flutter
```zsh
flutter clean
flutter pub get
```

## set up java version (for now 17 works best)
why: if you get "Unsupported class file major version 67" from gradlew

java -version

if need to install a specific version: 
        sudo apt install openjdk-17-jdk

update-java-alternatives --list
sudo update-java-alternatives --set java-1.17.0-openjdk-amd64

to make change permanent, add to ~/.zshrc
        'export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64'
        'export PATH=$JAVA_HOME/bin:$PATH'
# Studio/gradle Guide

- from flutter project:
```bash
flutter clean
flutter pub get
```

- from home:
```bash
cd dev/android-studio/bin/
./studio
```

- wait until background tasks are done
- from settings: install new android studio version (may be several)
- run AGP Upgrade assistant

- refresh dependencies: 

```bash
cd android
./gradlew --refresh-dependencies
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
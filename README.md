# React Native Hello World on Android Emulator

Following guide at: <https://facebook.github.io/react-native/docs/getting-started.html>

Install: (latest version of node already have)

## Java

- `sudo apt-get install default-jre default-jdk`
- add to `~/.profile`

  ```
  export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/jre
  ```

## Android Studio

- add to `~/.profile`

  ```
  # Setup Android/React Native
  export PATH=$PATH:$HOME/android-studio/bin
  export ANDROID_HOME=$HOME/Android/Sdk
  ```

- install 32 bit libs (or ssd fails on virtual device)

  ```
  sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1u
  ```

- create and run a new android nougat device - note that this is android-24

## React

```
npm install -g react-native-cli
react-native init reactHelloWorld
cd reactHelloWorld
```

- modify the versions in `build.gradle`

```
vi android/app/build.gradle

// update line 85 to:
 android {
    compileSdkVersion 24
    buildToolsVersion "24.0.2"
```

Open a new tab in the react project
```
npm start
// or
react-native start
```

In original tab

```
react-native run-android
```

Note: for performance also install `watchman` https://facebook.github.io/watchman/docs/install.html#installing-from-source

(note only master branch at current time)

and `gradle deamon` https://docs.gradle.org/2.9/userguide/gradle_daemon.html



## Notes on work-flow.

Start the emulator without the studio! - `~/Android/Sdk/tools/emulator @Nexus_5_API_24`

Then run in `react-native start` and `react-native run-android`

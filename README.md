# react-native-boilerplate
React Native lets you build mobile apps using only JavaScript. This boilerplate is my personal base setup for all react-native apps I plan to create.

## Requirements
* Node/npm
 * react-native-cli (global install)
* Java SE Development Kit 8+
* Android development environment
 * android sdk
 * android sdk platform
 * android virtual device

## Install
```
npm install -g react-native-cli
npm install --save react react-native wordwrap

```

### Android SDK
* download SDK and extract to `/usr/local/share` directory.
* Define $ANDROID_SDK_ROOT in `~/.bash_profile`.

```
cd $ANDROID_HOME/tools/bin
sudo ./sdkmanager --verbose "build-tools;26.0.0" "emulator" "platform-tools" "system-images;android-24;default;x86"
sudo ./avdmanager list target - lists existing targets
./avdmanager --verbose create avd --name ANDROID_API_26 --tag "google_apis" --abi "x86_64" --package "system-images;android-26;google_apis;x86_64"
./emulator #avd_name ($ANDROID_HOME/tools)
```

## Usage
The idea is to not depend on `react-native init` to create apps. Follow the steps to start from scratch:
```
npm install
react-native upgrade
npm start
react-native run-android
```

## Dev notes
* **wordwrap** needs to be installed locally. For some reason `react-native-cli` has it as a missing module.

## References
1. https://facebook.github.io/react-native/docs/getting-started.html

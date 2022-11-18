# React Native CLI - cheat list
> This cheat list contain all necessary commands for React Native CLI

## Installation flow - Create new project macOS
<span id="create"></span>

Original documentation [Environment setup](https://reactnative.dev/docs/environment-setup)

### Node & Watchman
```
brew install node
brew install watchman
```
> for Android
### Java Development Kit
```
brew tap homebrew/cask-versions
brew install --cask zulu11
```
### Android development environment
1. Install Android Studio
2. Install the Android SDK
3. Configure the ANDROID_SDK_ROOT environment variable

Add the following lines to your $HOME/.bash_profile or $HOME/.bashrc (if you are using zsh then ~/.zprofile or ~/.zshrc) config file:
```
export ANDROID_SDK_ROOT=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_SDK_ROOT/emulator
export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools
```

> for iOS

### Ruby
install `rvm` - [link](https://rvm.io/)

### Xcode
install the latest version of Xcode

### Installing an iOS Simulator in Xcode

### CocoaPods

`sudo gem install cocoapods`

### Creating a new application
``` 
npm uninstall -g react-native-cli @react-native-community/cli
npx react-native init <name_of_project>
```
or 
``` 
npx react-native init AwesomeTSProject --template react-native-template-typescript
```

Move to project folder

### Bundler
Move to ./ios folder and run`bundle install`

### Pod install
Move to ./ios folder and run `pod install`


## Installation flow - Clone existed project
<span id="clone"></span>
1. ...
2. ...
3. 

## General
<span id="general"></span>
`npm start` or `yarn start` or `npx react-native start` - start Metro server

`npm run android` or `yarn android` or `npx react-native run-android` - build and start Android emulator

`npm run ios` or `yarn ios` or `npx react-native run-ios` - build and start iOS emulator

## ~/ios
<span id="ios"></span>
> Run this commands only in folder `./ios`

`pod install` - install pods


## ~/android
<span id="android"></span>
> Run this commands only in folder `./android`

`./gradlew clean` - clean project


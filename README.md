# React Native Setup

For this homework you will be installing the React Native client on your computer and running the "Hello World" script.

## React Native for MAC OSX Only
** Note: This process will not work on a Windows Machine. 

In order to get started head over to: https://facebook.github.io/react-native/docs/getting-started.html and follow along with the instructions. Also be sure to note that there are different steps when installing for Android and IOS.

First thing you will need to do is install Node and Watchman:

```
brew install node
brew install watchman
```

After that you will need to install the React-Native-CLI:

```
npm install -g react-native-cli
```

Next tool that you are going to need is the XCode tool, which you can download from the App Store:

[XCode Can be found Here](https://itunes.apple.com/us/app/xcode/id497799835?mt=12)

Now go to your directory where you wish to create the project and then open the project up in XCode:

```
react-native init Hello-World
cd Hello-World
react-native run-ios  
```

This should open up the base template for your React Native project.

## React Native for Windows on Android

One important difference between Windows and Mac OSX when it comes to React Native is that while Mac can develop for both Android and IOS. Windows computer can only develop React Native for Android for the time being. 

Before you run the following commands you will need to install Chocolatey. The instructions on how to install Chocolatey can be found on their website:
[How to Install Chocolatey](https://chocolatey.org/install)

In order get started you will want to install Python2 and Node.js via the terminal: 
```
choco install nodejs.install
choco install python2
```

Once Node and Python are installed you can then install the React Native Command Line Interface.

```
npm install -g react-native-cli

```

Now that the Command Line Interface is installed you will need to install Android studio on your computer. Make sure to choose "Custom" installation when running Android Studio for the first time. Make sure the boxes next to all of the following are checked:

Android SDK
Android SDK Platform
Performance (Intel ® HAXM)
Android Virtual Device
Then, click "Next" to install all of these components.

[Android Studio Install](https://developer.android.com/studio/install.html)

### Android Studio Install Part 1

Android Studio installs the most recent Android SDK by default. React Native, however, requires the Android 6.0 (Marshmallow) SDK. To install it, launch the SDK Manager, click on "Configure" > "SDK Manager" in the "Welcome to Android Studio" screen.

```
The SDK Manager can also be found within the Android Studio "Preferences" menu, under Appearance & Behavior → System Settings → Android SDK.
```

Select the "SDK Platforms" tab from within the SDK Manager, then check the box next to "Show Package Details" in the bottom right corner. Look for and expand the Android 6.0 (Marshmallow) entry, then make sure the following items are all checked:

- Google APIs
- Android SDK Platform 23
- Intel x86 Atom_64 System Image
- Google APIs Intel x86 Atom_64 System Image

Next, select the "SDK Tools" tab and check the box next to "Show Package Details" here as well. Look for and expand the "Android SDK Build Tools" entry, then make sure that Android SDK Build-Tools 23.0.1 is selected.

Finally, click "Apply" to download and install the Android SDK and related build tools.

### Android Studio Install Part 2 

Set up the ANDROID_HOME environment variable 

The React Native command line interface requires the ANDROID_HOME environment variable to be set up.

```
Go to Control Panel → System and Security → System → Change settings → 
Advanced System Settings → Environment variables → 
New, then enter the path to your Android SDK.
```


Restart the Command Prompt to apply the new environment variable.

Please make sure you export the correct path for ANDROID_HOME if you did not install the Android SDK using Android Studio.

### Android Studio Install Part 3

You can see the list of available AVDs by opening the "AVD Manager" from within Android Studio. You can also run the following command in a terminal:

```
android avd
```
Once in the "AVD Manager", select your AVD and click "Edit...". Choose "Android 6.0 - API Level 23" under Device, and "Intel Atom (x86_64)" under CPU/ABI. Click OK, then select your new AVD and click "Start...", and finally, "Launch".


### Android Studio Install Part 4
Use the React Native command line interface to generate a new React Native project called "Hello-World", then run react-native start inside the newly created folder to start the packager.Now to create your project and open the newly create React Native App run the following in the terminal: 

```
react-native init Hello-World
cd Hello-World
react-native start

```

Open a new command prompt and run react-native run-android inside the same folder to launch the app on your Android emulator.

```
react-native run-android
```

If everything is set up correctly, you should see your new app running in your Android emulator shortly.


## Android Build:
For Android device there are two ways to build an app for release. The first way is through an APK
#### Create APK:
1. To create the APK, run the following command in the command line:
```
	flutter build apk --split-per-abi
```
2. Download the APK to your android device with a USB cable using the command line
	1. Connect your Android-powered device to your computer with a USB cable.
	2. Enter `cd [project]`.
	3. Run `flutter install`.
#### Create App Bundle: 
1. Enter `cd [project]`
2. Run `flutter build appbundle`
3. The release bundle for your app is created at `[project]/build/app/outputs/bundle/release/app.aab`
#### Google Play:
1. For deploying to Google Play follow: https://docs.flutter.dev/deployment/android
## IOS Build:
#### Create IPA:
1. To Create the IPA you have to run:
```
flutter build ipa
```
#### App Store:
1. For deploying to the App Store follow: https://docs.flutter.dev/deployment/ios
## Web Build:
1. For deploying to the Web follow: https://docs.flutter.dev/deployment/web
